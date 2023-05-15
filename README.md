## Action-RunScript

GitHub action to run yaml files 
<br></br>
[![CI](https://github.com/jge162/Action-RunScript/actions/workflows/Action-RunScript.yml/badge.svg)](https://github.com/jge162/Action-RunScript/actions/workflows/Action-RunScript.yml)
[![Create_Release](https://github.com/jge162/Action-RunScript/actions/workflows/CreateRelease.yml/badge.svg)](https://github.com/jge162/Action-RunScript/actions/workflows/CreateRelease.yml)
[![Dependabot auto-merge](https://github.com/jge162/Action-RunScript/actions/workflows/AutoMergeDependabot.yml/badge.svg)](https://github.com/jge162/Action-RunScript/actions/workflows/AutoMergeDependabot.yml)
[![Auto-merge Owner only](https://github.com/jge162/Action-RunScript/actions/workflows/AutoMerge.yml/badge.svg)](https://github.com/jge162/Action-RunScript/actions/workflows/AutoMerge.yml)
<br></br>
<img src="https://user-images.githubusercontent.com/31228460/218295872-1865b4ba-9c3c-4a28-bac8-0fd11c7c37f6.png" width="79%">

### Basic implementation using simple yml from GitHub  

```yaml
# This is a basic workflow to help you get started with Actions

name: Action-RunScript
run-name: ${{ github.head_ref }} (${{ github.actor }}) 🚀

# Controls when the workflow will run
on:
  # Triggers the workflow on push or pull request events but only for the "main" branch
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

# A workflow run is made up of one or more jobs that can run sequentially or in parallel
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: jge162/Action-RunScript@2.0.0

      # Runs a single command using the runners shell
      - name: Run a one-line script
        run: echo Hello, world!

      # Runs a set of commands using the runners shell
      - name: Run a multi-line script
        run: |
          echo Add other actions to build,
          echo test, and deploy your project.
```

License [Mit](https://github.com/jge162/Action-RunScript/blob/main/LICENSE)
