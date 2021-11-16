# The global `.github` for all OpenWonderLabs projects

This projects contains any sort of common and community health files for the OpenWonderLabs organization
to be maintained in a central space.

## Reusable GitHub Workflows

This project provides several GitHub workflows that can be [reused](https://docs.github.com/en/actions/learn-github-actions/reusing-workflows).

This example, which is cited from the above-linked GitHub documentation page, shows how such
reusable workflow files are generally used: 

```yaml
name: Call a reusable workflow

on:
  pull_request:
    branches:
      - main

jobs:
  call-workflow:
    uses: OpenWonderLabs/.github/.github/workflows/example-workflow.yml@main

  call-workflow-passing-data:
    uses: OpenWonderLabs/.github/.github/workflows/example-workflow.yml@main
    with:
      username: mona
    secrets:
      token: ${{ secrets.TOKEN }}
```
