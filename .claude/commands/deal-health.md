---
description: Assess deal completeness and health by scanning for missing critical information across all artifacts.
---
Run a deal health check.

Argument: $ARGUMENTS is the account name (optional - if not provided, use current context).

Steps:
1) Locate the deal folder: deals/$ARGUMENTS/[most recent date]/
2) Scan all files in inputs/ and outputs/ folders
3) Check for the following critical elements across all artifacts:
   - Economic buyer identified (name + role)
   - Decision timeline with specific date
   - Quantified success criteria (with numbers)
   - Implementation owner identified
   - Budget/pricing discussed
   - Integration requirements documented
   - Security/compliance requirements documented
   - Competitive landscape noted
4) Generate a health report with three sections:
   - GREEN: Critical elements present and complete
   - YELLOW: Critical elements present but vague/incomplete
   - RED: Critical elements missing entirely
5) Create a "What We Still Need" action list with specific questions to ask
6) Output to: deals/$ARGUMENTS/[date]/outputs/deal-health-report.md

Format the report as:
# Deal Health Report - [Account] - [Date]

## Health Score: [RED/YELLOW/GREEN]

## GREEN ✓ (Complete)
- [list items]

## YELLOW ⚠ (Incomplete)
- [list items with what's missing]

## RED ✗ (Missing)
- [list items]

## What We Still Need (Priority Order)
1. [Specific question/action]
2. [Specific question/action]
...

## Recommendation
[One sentence: ready to proceed / need more discovery / at risk]
