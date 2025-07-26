# Simple CI Pipeline with GitHub Actions 🐜🍃

A hands-on beginner project that introduces a basic Continuous Integration (CI) workflow using **GitHub Actions**. This pipeline automatically runs tests and validation checks on every push and pull request—helping developers build with confidence, consistency, and automation in mind.

---

## Project Objectives

- Set up a basic CI workflow using GitHub Actions
- Trigger pipeline on code pushes and pull requests
- Run automated test scripts (e.g., unit tests, linter)
- Learn the foundations of DevOps automation via GitHub

---

## Technologies Used

- **Git & GitHub**
- **GitHub Actions**
- **YAML Workflows**
- *(Optional)* Node.js / Python / Shell Scripts – for demo purposes

---

## Folder Structure

```bash
.
├── .github/
│   └── workflows/
│       └── ci.yml         # Main GitHub Actions workflow
├── src/                   # Sample source code or logic
├── test/                  # Sample test files
└── README.md              # Project overview and instructions

---

⚙️ How It Works

1. Every time you push or create a pull request, GitHub triggers the CI workflow.

2. The workflow runs a predefined set of steps:
- Checkout repository
- Set up the environment
- Install dependencies
- Run tests or linters

3. Results are shown in the Actions tab of your GitHub repo.

---

⚗️ Sample Workflow: .github/workflows/ci.yml

name: CI Pipeline

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build-and-test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v4

      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'

      - name: Install Dependencies
        run: npm install

      - name: Run Tests
        run: npm test

 > You can easily modify this to fit any tech stack: Python, Go, Java, etc.

---

🐜 Learning Outcome

By completing this project, you will:
- Understand the flow of GitHub Actions
- Automate test validation on every code change
- Set the stage for more advanced CI/CD pipelines

Part of the Series
This project is part of the Zero-to-Git-Hero series:
A hands-on collection of DevOps & GitHub automation projects for beginners.

> View the full project list: https://github.com/ricoaprillananda/zero-to-git-hero

---

🧾  License

MIT License © 2025 Rico Aprilla
Feel free to fork, contribute, and learn! 







