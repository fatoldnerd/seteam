---
description: Synthesize notes from any call (discovery, demo, technical, executive) and update the running deal context with what changed.
---
Synthesize call notes and track deal progression.

Argument: $ARGUMENTS is the account name.

Steps:
1) Locate the most recent deal folder: deals/$ARGUMENTS/[most recent date]/
2) Look for the newest call notes file in inputs/ (e.g., call-notes.md, call-01-discovery.md, etc.)
3) Read all existing outputs to understand the current state of the deal
4) Analyze the new call notes for:
   - New information learned (pain, stakeholders, timeline, budget, success criteria)
   - Changes from previous understanding (what shifted, what got clarified)
   - Contradictions or inconsistencies with earlier artifacts
   - New risks or blockers that emerged
   - Commitments made (by them or by us)
5) Generate three outputs:

   A) deals/$ARGUMENTS/[date]/outputs/call-synthesis-[callnumber].md with:
      # Call Synthesis - [Account] - [Date] - Call [#]
      
      ## Call Type
      [Discovery / Demo / Technical / Executive / Combined]
      
      ## What We Learned (New Information)
      - [Bulleted list of net-new facts]
      
      ## What Changed (Updates to Previous Understanding)
      - [What we thought before] → [What we know now]
      
      ## What's Now Clear (Previously Unclear)
      - [Items that moved from assumption/TBC to confirmed]
      
      ## What's Still Unclear (Gaps Remaining)
      - [Critical unknowns, prioritized]
      
      ## New Risks or Blockers
      - [What emerged that could derail the deal]
      
      ## Commitments Made
      - Us: [What we promised to do/deliver]
      - Them: [What they committed to]
      
      ## Next Actions (Specific, Owned, Dated)
      1. [Action] - [Owner] - [Due date]
      2. [Action] - [Owner] - [Due date]

   B) Update or create deals/$ARGUMENTS/[date]/outputs/current-deal-state.md with:
      # Current Deal State - [Account] - [Updated: Date]
      
      ## Deal Snapshot (1-2 sentences)
      [Where we are, what stage, what's happening next]
      
      ## Confirmed Facts
      - Economic buyer: [Name, role]
      - Champion: [Name, role]
      - Decision timeline: [Specific date or timeframe]
      - Budget: [Confirmed/TBC/Amount]
      - Success criteria: [Specific, measurable]
      - Implementation owner: [Name, role or TBC]
      - Key integrations: [List]
      - Security/compliance requirements: [List]
      
      ## Deal Momentum: [ACCELERATING / STEADY / STALLING / AT RISK]
      Rationale: [One sentence explaining the momentum assessment]
      
      ## Critical Path to Close
      1. [Next milestone] - [Date]
      2. [Next milestone] - [Date]
      3. [Close target] - [Date]
      
      ## Open Risks (Prioritized)
      1. [Risk] - [Mitigation plan]
      2. [Risk] - [Mitigation plan]

   C) Generate deals/$ARGUMENTS/[date]/outputs/what-changed-summary.txt (plain text, AE-friendly):
      Short summary (3-5 bullets max) of what's different after this call.
      Format for quick Slack/email: "After today's call with [Account]:"

Rules:
- If this is the first call, focus on "What We Learned" (no "What Changed" section)
- If discovery and demo happened on same call, note both in Call Type
- Be specific: "Timeline moved from Q1 to end of February" not "Timeline got clearer"
- Flag assumptions that are still assumptions even after the call
- If the AE ran the demo, note that in the synthesis
- Keep what-changed-summary.txt under 100 words (for quick sharing)
