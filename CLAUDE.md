# Claude Code Rules:
# SE Team Workspace (Claude Code)

## Purpose
A shared workspace for Sales Engineering to produce consistent, high-quality artifacts:
- Discovery synth + next steps
- Demo plan + talk track + success criteria
- Security/compliance responses
- Executive brief + value narrative
- Implementation handoff

## Deal workflow (required)
1) /new-deal <Account>
2) Update inputs/deal-context.md
3) Add call notes for each interaction:
   - call-01-discovery.md
   - call-02-demo.md
   - call-03-technical.md
   - call-04-exec.md
4) After each call, run:
   - /call-synthesis <Account>
   - /deal-health <Account>


## Non-negotiable rules
1) Tie everything to the customer’s operational workflow and measurable outcomes.
2) Never invent product capabilities. If unknown, add an explicit “Assumption” section.
3) Use templates from /templates whenever a matching template exists.
4) Store outputs in the current deal folder: /deals/<account>/<yyyymmdd>/outputs/
5) Do NOT commit sensitive customer data to git. Use /deals/**/private/ or CLAUDE.local.md.

## Source of truth
- Product + company context: /context/
- Templates: /templates/
- Playbooks: /playbooks/

## Subagent routing hints (who to delegate to)
- deal-researcher: pre-call account + industry + competitor context
- discovery-synthesizer: turn transcript/notes into a crisp discovery summary
- demo-architect: turn discovery into a demo flow + talk track + success criteria
- security-responder: draft security answers + data-flow narrative without over-claiming
- handoff-writer: implementation handoff with scope, integrations, risks, acceptance criteria

Think through the problem, read the codebase for relevant files, and write a plan to tasks/todo.md.
The plan should have a list of todo items that you can check off as you complete them
Before you begin working, check in with me and I will verify the plan.
Then, begin working on the todo items, marking them as complete as you go.
Please every step of the way just give me a high level explanation of what changes you made
Make every task and code change you do as simple as possible. We want to avoid making any massive or complex changes. Every change should impact as little code as possible. Everything is about simplicity.
Finally, add a review section to the todo.md file with a summary of the changes you made and any other relevant information.
DO NOT BE LAZY. NEVER BE LAZY. IF THERE IS A BUG FIND THE ROOT CAUSE AND FIX IT. NO TEMPORARY FIXES. YOU ARE A SENIOR DEVELOPER. NEVER BE LAZY
MAKE ALL FIXES AND CODE CHANGES AS SIMPLE AS HUMANLY POSSIBLE. THEY SHOULD ONLY IMPACT NECESSARY CODE RELEVANT TO THE TASK AND NOTHING ELSE. IT SHOULD IMPACT AS LITTLE CODE AS POSSIBLE. YOUR GOAL IS TO NOT INTRODUCE ANY BUGS. IT'S ALL ABOUT SIMPLICITY
