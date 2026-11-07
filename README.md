<<<<<<< HEAD
<<<<<<< HEAD
# Lab 06: Your First Continuous Integration (CI) Pipeline

- **Student Name:** Ali Ul Murtaza Alvi
- **Registration Number:** 23-NTU-CS-FL-1244
- **Course:** DevOps
- **Repository:** [devops-project-faisal-ali](https://github.com/aliulmurtazaalvi/devops-project-faisal-ali)

---

## Overview
This repository contains the implementation of Lab 06, focusing on establishing an automated Continuous Integration (CI) workflow with GitHub Actions, performing intentional failure validation, and configuring branch protection rulesets to act as a rigorous status check gate.

---

## Pipeline Architecture (`.github/workflows/ci.yml`)
The CI pipeline triggers automatically on pushes and pull requests targeting the `main` branch, as well as via a scheduled nightly dependency audit (`0 2 * * *`).

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
  schedule:
    - cron: '0 2 * * *'

jobs:
  build:
    name: build-and-test
    runs-on: ubuntu-24.04
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
        with:
          node-version: '22'
          cache: npm
      - name: Build, test and package
        run: make ci
      - uses: actions/upload-artifact@v4
        with:
          name: devops-pipeline
          path: '*.tgz'
          if-no-files-found: error
=======
# devops-project-faisalandali
>>>>>>> e8ab4af (Initial commit)
=======
- Ali Ul Murtaza Alvi (23-NTU-CS-FL-1244)
- Mirza M. Faisal Baig (23-NTU-CS-FL-1175)
Reviews must be answered within 24 hours (one working day).
>>>>>>> 8adfe8e (Initialize project documentation and gitignore)
