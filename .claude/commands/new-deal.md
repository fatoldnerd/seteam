---
description: Create a new deal workspace under /deals/<account>/<yyyymmdd>/ with standard inputs/outputs.
---
Create a new deal workspace.


Argument: $ARGUMENTS is the account name.


Steps:
1) Create deals/$ARGUMENTS/$(date +%Y%m%d)/inputs and outputs.
2) Copy deals/_template/inputs/deal-context.md into the new inputs folder.
3) Confirm the final path.
