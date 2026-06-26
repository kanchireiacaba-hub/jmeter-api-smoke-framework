# 🚀 JMeter API Smoke Testing Framework

> A CI/CD-ready API smoke testing framework built with Apache JMeter and GitHub Actions.

## 📖 Overview

This project demonstrates how to automate API smoke testing using **Apache JMeter** and integrate it with **GitHub Actions** for continuous testing.

The framework automatically:

* Executes API smoke tests
* Generates HTML dashboard reports
* Uploads test artifacts
* Supports scheduled execution (Monday–Friday, 8:00 AM PHT)
* Provides a foundation for email and Microsoft Teams notifications

---

# 🏗 Architecture

```
Developer
     │
git push
     │
     ▼
GitHub Repository
     │
     ▼
GitHub Actions
     │
     ▼
Install Java
     │
     ▼
Download Apache JMeter
     │
     ▼
Execute Smoke Tests
     │
     ▼
Generate HTML Dashboard
     │
     ▼
Upload HTML Report
     │
     ▼
(Upcoming)
Email Notification
     │
     ▼
Microsoft Teams Notification
```

---

# 📁 Project Structure

```
jmeter-api-smoke-framework
│
├── .github
│   └── workflows
│       └── smoke-test.yml
│
├── jmeter
│   └── Smoke-API.jmx
│
├── data
│
├── reports
│
├── results
│
├── README.md
│
└── .gitignore
```

---

# ⚙️ Tech Stack

| Technology     | Purpose           |
| -------------- | ----------------- |
| Apache JMeter  | API Automation    |
| GitHub Actions | CI/CD Pipeline    |
| Java 17        | Runtime           |
| Git            | Version Control   |
| GitHub         | Source Repository |

---

# ✅ Smoke Test Coverage

Current automated flow:

1. Login
2. Extract JWT Token
3. Get Current User
4. Create Post
5. Update Post
6. Delete Post

Concepts demonstrated:

* HTTP Request Defaults
* HTTP Header Manager
* JSON Extractor
* Correlation
* Assertions
* Variables
* Authentication
* HTML Dashboard Reporting

---

# ▶️ Running Locally

Run the test in non-GUI mode:

```bash
jmeter -n \
-t jmeter/Smoke-API.jmx \
-l results/results.jtl \
-e \
-o reports
```

Open:

```
reports/index.html
```

to view the HTML dashboard.

---

# ⚙️ GitHub Actions

The workflow automatically executes:

* On every push to the `main` branch
* Manually using **Run workflow**
* Every **Monday–Friday at 8:00 AM Philippine Time**

Workflow:

```
Checkout Repository
        ↓
Install Java
        ↓
Download JMeter
        ↓
Execute Smoke Test
        ↓
Generate HTML Report
        ↓
Upload Report Artifact
```

---

# 📊 HTML Report

The generated dashboard includes:

* Response Time
* Error Percentage
* Throughput
* APDEX
* Transactions
* Active Threads
* Assertions

---

# 📷 Screenshots

## GitHub Actions

> *(Add a screenshot of a successful GitHub Actions workflow here.)*

---

## HTML Dashboard

> *(Add a screenshot of the generated JMeter HTML report here.)*

---

# 🚀 Future Enhancements

* CSV Data-Driven Testing
* Environment Configuration
* Automatic Email Notifications
* Microsoft Teams Integration
* Docker Support
* Performance Testing Pipeline
* Multi-environment Execution

---

# 👨‍💻 Author

Developed by **Kanchi Rei Acaba**

Automation QA Engineer

Focused on API Testing, UI Automation, CI/CD, and Test Automation Frameworks.
