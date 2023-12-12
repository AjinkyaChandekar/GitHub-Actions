## GitHub-Actions
Notes: https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows
###########**SYNTAX**###########
**ON**
**1. Using a single event**
For example, a workflow with the following on value will run when a **push is made to any branch** in the workflow's repository:

on: push

**2. Using multiple events**

on: [push, fork]

**3. Using activity types**
Use **on.<event_name>.types** (issue/label) to define the type of event activity that will trigger a workflow run.

on:
  label:
    types:
      - created
      - edited
      - deleted
 on:
  issues:
    types:
      - opened
      - labeled
      - deleted
      - milestoned
      
**2.on.workflow_dispatch**
  # Triggers the workflow on push or pull request events but only for the "env/prd" branch
  push:
    branches: [ "env/prd" ]
  pull_request:
    branches: [ "env/prd" ]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

  ![image](https://github.com/AjinkyaChandekar/GitHub-Actions/assets/65499227/6729d9f1-cd6e-4beb-86bd-fc16c5b0b5b8)

Note: Once you delete workflow yaml file, that workflow will be removed from Action tab.

**3.How to refer github.event ?** (It prints all events)
"issue": {
    "author_association": "OWNER",
    "body": "ABC",
    "number": 3,
    }
    
${{ github.event.issue.number }}
