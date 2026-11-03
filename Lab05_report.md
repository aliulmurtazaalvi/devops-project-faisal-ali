# DevOps Principles and Practices (2+1)
## Lab 05 Report: Builds, Dependencies and Versioned Artifacts

**Team Name:** team-faisal-ali  
**Date:** October 20, 2026  
**Environment:** WSL2 (Ubuntu 24.04 LTS), Node.js v24.22.0  

### Team Members & Submission Metadata
* **Member 1 (Lead / Packager):** Ali Ul Murtaza Alvi (Reg No: 23-NTU-CS-FL-1244 | GitHub: [@aliulmurtazaalvi](https://github.com/aliulmurtazaalvi))
* **Member 2 (Partner / Reviewer):** Mirza Faisal (Email: mirzafaisal.99fb@gmail.com | GitHub: [@mirzafaisal99fb-sudo](https://github.com/mirzafaisal99fb-sudo))
* **Team Repository:** [https://github.com/aliulmurtazaalvi/devops-project-faisal-ali](https://github.com/aliulmurtazaalvi/devops-project-faisal-ali)
* **Team Pull Request:** [https://github.com/aliulmurtazaalvi/devops-project-faisal-ali/pull/1](https://github.com/aliulmurtazaalvi/devops-project-faisal-ali/pull/1)
* **Published Package (GitHub Packages):** [https://github.com/aliulmurtazaalvi?tab=packages](https://github.com/aliulmurtazaalvi?tab=packages)
* **Package Scope & Name:** `@aliulmurtazaalvi/devops-pipeline`

---

### 1. Dependency Analysis & Diamond Resolution (Task 1)
* **Direct vs Transitive Dependencies:**  
  Declaring 1 direct runtime dependency (`markdown-it`) resulted in **7 total packages** installed in `node_modules` (1 direct, 6 transitive).
* **Terminal Dependency Tree (`npm ls --all`):**
```text
devops-pipeline@1.0.0 /home/ali_alvi_1244/devops/lab05
`-- markdown-it@15.0.3
  +-- argparse@3.0.3
  +-- entities@8.1.0
  +-- linkify-it@6.1.0
  | `-- uc.micro@3.0.0 deduped
  +-- mdurl@2.1.0
  +-- punycode.js@2.3.1
  `-- uc.micro@3.0.0
