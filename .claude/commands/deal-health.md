---
description: Assess deal completeness by scanning the most recent deal folder for missing critical info and producing a RED/YELLOW/GREEN report.
---

Run a deal health check.

Input:
- $ARGUMENTS = account name (required)

Steps:
1) Locate the most recent deal folder for the account:
   - Base path: deals/$ARGUMENTS/
   - Choose the newest date folder by lexicographic sort (YYYYMMDD).
2) Scan all files in that folder’s inputs/ and outputs/.
3) Determine presence + specificity for each element:

HARD GATES (must be present for anything above RED)
- Economic buyer: name + role
- Decision timeline: specific date or clear target window
- Success criteria: at least 2 measurable metrics

MEDIUM ITEMS
- Implementation owner: name + role (or clearly assigned team)
- Budget/pricing: confirmed amount OR confirmed owner + planned next step
- Integrations: named systems + what direction of data flow is needed
- Security/compliance: named requirements + owner/nexstep
- Competition: named competitor(s) OR explicit “no competitor identified”

4) Score:
- RED if any HARD GATE is missing.
- YELLOW if HARD GATES exist but any are vague, or 2+ MEDIUM ITEMS missing.
- GREEN if HARD GATES are specific and fewer than 2 MEDIUM ITEMS missing.

5) Output a report to:
   deals/$ARGUMENTS/<date>/outputs/deal-health-report.md

Report format:
# Deal Health Report — $ARGUMENTS — <date>

## Health Score: RED | YELLOW | GREEN

## GREEN ✓ (Complete)
-

## YELLOW ⚠ (Present but incomplete)
- Item: what’s missing / what to clarify

## RED ✗ (Missing)
-

## What We Still Need (Priority Order)
1) Specific question to ask / action to take

## Recommendation
One sentence: proceed / run more discovery / at risk
