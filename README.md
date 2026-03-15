# helloWorld

A minimal starter repository used to explore and validate GitHub basics, including pushing commits and setting up GitHub Actions CI workflows.

## Features

- Boilerplate GitHub Actions CI workflow that triggers on pushes and pull requests to `main`
- Manually triggered GitHub Actions workflow that accepts a name input and prints a greeting
- Scratch file used to verify push functionality

## Prerequisites

- [Git](https://git-scm.com/) (any recent version)
- A GitHub account (to trigger and view workflow runs)

## Installation

Clone the repository:

```bash
git clone https://github.com/KaizenXIII/helloWorld.git
cd helloWorld
```

No build steps, package managers, or runtimes are required.

## Usage

### CI Workflow (automatic)

The `CI` workflow (`.github/workflows/blank.yml`) runs automatically on every push or pull request targeting the `main` branch. It checks out the repository and echoes a greeting to confirm the runner is working.

To trigger it manually from the GitHub UI, navigate to **Actions > CI > Run workflow**.

### Manual Greeting Workflow

The `Manual workflow` (`.github/workflows/manual.yml`) is triggered exclusively through the GitHub Actions UI or API.

1. Go to **Actions > Manual workflow > Run workflow**.
2. Enter a name in the **Person to greet** field (defaults to `World`).
3. Click **Run workflow**.

The job will print:

```
Hello <name>
```

## Project Structure

```
helloWorld/
├── .github/
│   └── workflows/
│       ├── blank.yml      # Automatic CI workflow (push / PR trigger)
│       └── manual.yml     # Manually dispatched greeting workflow
└── testPush.txt           # Scratch file used to test git push
```

## Development

This repository has no build system or test suite. To experiment:

1. Edit any file or add a new one.
2. Commit and push to `main` to observe the CI workflow run in GitHub Actions.

## License

No license file is currently present in this repository. Add one at the root (e.g., `LICENSE`) to declare the terms under which others may use or contribute to the project.
