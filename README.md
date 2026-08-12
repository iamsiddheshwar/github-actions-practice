# GitHub Actions Learning 🚀

This repository contains my hands-on practice with **GitHub Actions** and **Continuous Integration (CI)**.

The goal of this repository is to understand how GitHub Actions workflows are created, triggered, and executed using YAML configuration files.

## 📌 What I Learned

Through this practical, I learned:

* What GitHub Actions is
* What a workflow is
* How workflows are triggered
* How the `push` event triggers a workflow
* How to create workflow files using YAML
* How jobs work inside a workflow
* How steps work inside jobs
* How GitHub-hosted runners execute jobs
* How multiple jobs can be defined in a single workflow
* How CI automation works when changes are pushed to a repository

## 📂 Repository Structure

```text
github-actions-learning/
│
├── .github/
│   └── workflows/
│       └── my-workflow.yaml
│
└── README.md
```

## ⚙️ My First Workflow

The workflow is located at:

```text
.github/workflows/my-workflow.yaml
```

The workflow is triggered whenever code is pushed to the repository:

```yaml
on: push
```

It contains two jobs:

```text
Workflow
│
├── job-1
│   ├── step-1
│   └── step-2
│
└── job-2
    ├── final step
    └── another step
```

Each job runs on:

```yaml
runs-on: ubuntu-latest
```

## 🔄 How the Workflow Works

The basic execution flow is:

```text
Developer makes changes
        ↓
      git push
        ↓
GitHub detects the push
        ↓
Workflow is triggered
        ↓
Jobs are created
        ↓
Steps are executed
        ↓
Commands run on GitHub runner
        ↓
Workflow result is displayed
```

## 🧩 Important Concepts

### Workflow

A workflow is an automated process defined using a YAML file.

### Event

An event determines **when the workflow should run**.

Example:

```yaml
on: push
```

This means the workflow runs when changes are pushed to the repository.

### Job

A job is a group of steps that execute together on a runner.

Example:

```yaml
jobs:
  job-1:
    runs-on: ubuntu-latest
```

### Step

A step performs an individual task or command.

Example:

```yaml
steps:
  - name: step-1
    run: echo "Hello from step-1"
```

### Runner

A runner is the environment where the job executes.

In this practical, I used:

```yaml
runs-on: ubuntu-latest
```

which uses a GitHub-hosted Ubuntu runner.

## 🎯 Practical Objective

The main objective of this practical was to understand the basic structure of a GitHub Actions CI workflow:

```text
Workflow
   ↓
Event
   ↓
Jobs
   ↓
Steps
   ↓
Commands
   ↓
Runner
```

## 🛠️ Technologies Used

* Git
* GitHub
* GitHub Actions
* YAML
* Ubuntu
* Continuous Integration (CI)

## 🚀 Next Steps

I plan to extend this repository by practicing:

* Running automated tests
* Building applications with GitHub Actions
* Using environment variables
* Using GitHub Secrets
* Docker image builds
* Docker Hub integration
* CI/CD pipelines
* Deployment automation
* AWS integration

---

### 📚 Learning Journey

This repository is part of my ongoing **Cloud & DevOps learning journey**, where I am practicing concepts through hands-on implementation rather than only theoretical learning.

**Learn → Practice → Troubleshoot → Automate → Improve 🚀**
