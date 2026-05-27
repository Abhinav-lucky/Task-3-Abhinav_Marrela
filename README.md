# 🚀 Task 3 — CI/CD Pipeline Basics

> A CI/CD Pipeline built with **GitHub Actions** that automatically builds, tests, and deploys a static website to **GitHub Pages** as part of the **DecodeLabs DevOps Internship – Batch 2026**.

---

## 🌐 Live Demo

> **[https://Abhinav-lucky.github.io/Task-3-Abhinav_Marrela](https://Abhinav-lucky.github.io/Task-3-Abhinav_Marrela)**

---

## 📌 Project Overview

This project is part of **Project 3: CI/CD Pipeline Basics** under the DecodeLabs Industrial Training Kit. The goal was to build an **automated software delivery pipeline** that eliminates manual deployment — every `git push` triggers the entire pipeline automatically.

| Detail | Info |
|---|---|
| **Intern** | Abhinav Marrela |
| **Role** | DevOps Engineer Intern |
| **Organization** | DecodeLabs |
| **Batch** | 2026 |
| **Project** | Task 3 — CI/CD Pipeline Basics |

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Static website structure |
| CSS3 | Styling and layout |
| Git & GitHub | Version control & remote repository |
| GitHub Actions | CI/CD Pipeline automation |
| GitHub Pages | Free live deployment hosting |
| YAML | Pipeline configuration language |

---

## 📁 Project Structure

```
Task-3-Abhinav_Marrela/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml             # GitHub Actions pipeline config
│
├── index.html                    # Main webpage
├── style.css                     # Stylesheet
├── .gitignore                    # Excludes OS, editor & env files
└── README.md                     # Project documentation
```

---

## ⚙️ CI/CD Pipeline Architecture

The pipeline follows the **IPO Model** (Input → Process → Output):

```
git push (Trigger)
      │
      ▼
┌─────────────┐
│  BUILD      │  Checks out code & verifies project files
└──────┬──────┘
       │
       ▼
┌─────────────┐
│   TEST      │  Validates HTML, CSS & workflow files exist
└──────┬──────┘
       │
       ▼
┌─────────────┐
│  DEPLOY     │  Deploys live to GitHub Pages automatically
└─────────────┘
       │
       ▼
🌐 Live Website
```

---

## 🔄 Pipeline Stages Explained

### Stage 1 — Build
- Triggered on every `git push` to `main`
- Checks out the latest code
- Verifies all project files are present
- Runs on a fresh `ubuntu-latest` cloud runner

### Stage 2 — Test
- Runs only after Build passes
- Validates `index.html` exists
- Validates `style.css` exists
- Validates `ci-cd.yml` workflow file exists
- Fails and blocks deployment if any file is missing

### Stage 3 — Deploy
- Runs only after Test passes
- Configures GitHub Pages environment
- Uploads project as a deployment artifact
- Deploys live to GitHub Pages URL
- Outputs the live website URL

---

## 📋 Pipeline Configuration

```yaml
name: CI/CD Pipeline - DecodeLabs Project 3

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
  test:
    needs: build
    runs-on: ubuntu-latest
  deploy:
    needs: test
    runs-on: ubuntu-latest
```

---

## ✅ Pipeline Status

| Stage | Status |
|---|---|
| Build | ✅ Passing |
| Test | ✅ Passing |
| Deploy | ✅ Passing |

---

## 🖥️ Installation & Setup

```bash
# Step 1: Clone the repository
git clone https://github.com/Abhinav-lucky/Task-3-Abhinav_Marrela.git

# Step 2: Navigate into the project folder
cd Task-3-Abhinav_Marrela

# Step 3: Open locally in browser
start index.html        # Windows
open index.html         # Mac
xdg-open index.html     # Linux
```

---

## 🔐 .gitignore Coverage

```
# OS Files
.DS_Store
Thumbs.db

# Editor Files
.vscode/
.idea/

# Log Files
*.log

# Temp Files
*.tmp
*.temp

# Environment Files
.env
.env.local
```

---

## 💡 Key Learnings

- CI/CD is not about manual updates — it's about **Efficiency and Reliability**
- GitHub Actions uses **YAML** to define automated workflows
- Every pipeline follows **Build → Test → Deploy** stages
- The **GREEN CHECKMARK** means your code is verified and live
- A single `git push` results in a **secure, tested, automated deployment**

---

## 🔁 Connection to Previous Projects

| Project | Purpose |
|---|---|
| Task 1 | Linux & Shell Scripting Basics |
| Task 2 | Version Control with Git & GitHub |
| **Task 3** | **CI/CD Pipeline with GitHub Actions** |
| Task 4 | Coming Soon... |

---

## 📞 Contact

| Platform | Link |
|---|---|
| 💼 LinkedIn | [linkedin.com/in/lucky-abhinav](https://www.linkedin.com/in/lucky-abhinav/) |
| 🐙 GitHub | [github.com/Abhinav-lucky](https://github.com/Abhinav-lucky) |

---

## 📄 License

```
MIT License
Copyright (c) 2026 Abhinav Marrela
Permission is hereby granted, free of charge, to any person obtaining
a copy of this software to use, copy, modify, merge, publish, and
distribute it, subject to the following conditions: The above copyright
notice shall be included in all copies or substantial portions of the software.
```

---

<div align="center">

**Built with 💻 by Abhinav Marrela | DecodeLabs DevOps Intern – Batch 2026**

⭐ Star this repo if you found it helpful!

</div>
