---
description: Synthesize notes from a call and update the running deal state with what changed.
---

Synthesize call notes and track deal progression.

Input:
- $ARGUMENTS = account name (required)

Steps:
1) Locate the most recent deal folder for the account (same rule as deal-health).
2) Identify the newest call notes file in inputs/:
   - Prefer names like: call-01-discovery.md, call-02-demo.md, call-03-technical.md, call-notes.md
   - If multiple exist, choose the most recently modified.
3) Read existing outputs (if present):
   - outputs/current-deal-state.md
   - outputs/discovery-summary.md
   - outputs/demo-plan.md
   - outputs/deal-health-report.md (if present)
4) Analyze the new call notes for:
   - NEW facts learned
   - CHANGES from prior understanding (before → after)
   - CLARIFIED items (moved from assumption/TBC to confirmed)
   - REMAINING GAPS (prioritized)
   - RISKS / blockers
   - COMMITMENTS (us/them)
5) Create 3 outputs:

A) tputs/call-synthesis-<YYYYMMDD>-<shortlabel>.md
- Call Type: Discovery | Demo | Technical | Executive | Combined
- What We Learned (New)
- What Changed (Before → Now)
- What’s Now Clear
- What’s Still Unclear
- New Risks/Blockers
- Commitments Made (Us/Them)
- Next Actions (Owned + dated)

B) Update outputs/current-deal-state.md
- Deal Snapshot (1–2 sentences)
- Confirmed Facts (economic buyer, champion, timeline, budget, success criteria, impl owner, integrations, security)
- Deal Momentum: ACCELERATING | STEADY | STALLING | AT RISK (1-sentence rationale)
- Critical Path to Close (milestones + dates)
- Open Risks (prioritized + mitigation)

C) outputs/what-changed-summary.txt
- Under 100 words
- 3–5 bullets max
- Must include “Next step:”

Rules:
- If this is the first call, minimize “What Changed” and focus on “What We Learned.”
- If AE-led, note it explicitly.
- If discovery + demo both happened, label Call Type as Combined.
- Do not invent facts; label assumptions.
