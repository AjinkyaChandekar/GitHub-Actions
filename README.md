# GitHub-Actions
**on.workflow_dispatch**
on:
  # Triggers the workflow on push or pull request events but only for the "env/prd" branch
  push:
    branches: [ "env/prd" ]
  pull_request:
    branches: [ "env/prd" ]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

  ![image](https://github.com/AjinkyaChandekar/GitHub-Actions/assets/65499227/6729d9f1-cd6e-4beb-86bd-fc16c5b0b5b8)

Note: Once you delete workflow yaml file, that workflow will be removed from Action tab.
