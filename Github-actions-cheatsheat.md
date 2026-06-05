# GitHub Actions Cheat Sheet 🚀

## What is GitHub Actions?
GitHub Actions is GitHub's automation platform for CI/CD.

## CI/CD Flow
```text
Push Code
    ↓
Trigger
    ↓
Workflow
    ↓
Job
    ↓
Runner
    ↓
Steps
    ↓
Build
    ↓
Test
    ↓
Deploy
```

## Core Concepts

### Workflow
Complete automation process.

### Event (Trigger)
Starts the workflow.
- push
- pull_request
- workflow_dispatch
- schedule

### Job
Major task such as Build, Test, Deploy.

### Runner
Temporary machine that executes jobs.
- ubuntu-latest
- windows-latest
- macos-latest

### Step
Small action inside a job.

### Action
Reusable automation.
Example:
```yaml
uses: actions/checkout@v4
```

## uses vs run

### uses
Use an existing action.
```yaml
uses: actions/checkout@v4
```

### run
Run your own command.
```yaml
run: echo "Hello World"
```

## Most Important Keywords

| Keyword | Purpose |
|----------|----------|
| name | Workflow name |
| on | Trigger |
| jobs | Define jobs |
| runs-on | Runner machine |
| steps | Task list |
| uses | Existing action |
| run | Execute command |
| env | Environment variables |
| secrets | Secure values |

## Secrets
```yaml
${{ secrets.MY_SECRET }}
```

## Schedule
```yaml
on:
  schedule:
    - cron: "0 9 * * *"
```

## Manual Run
```yaml
on:
  workflow_dispatch:
```

## Workflow Structure

```yaml
name: My Workflow

on:
  push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Run Command
        run: echo "Hello"
```

## Quick Interview Revision

- CI = Build + Test Automatically
- CD = Deploy Automatically
- Workflow = Entire Automation
- Event = Trigger
- Job = Major Task
- Runner = Machine
- Step = Small Task
- Action = Reusable Automation
- uses = Existing Action
- run = Custom Command

## Memory Formula

```text
Workflow
   ↓
Event
   ↓
Job
   ↓
Runner
   ↓
Steps
   ↓
Action / Run
```
