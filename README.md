# API Smoke Testing Framework

## Tech Stack

- Apache JMeter
- GitHub Actions
- HTML Dashboard

## Features

- Login API
- Token Correlation
- Authenticated Requests
- CRUD Smoke Tests
- HTML Dashboard
- Scheduled Execution
- Email Notification
- Microsoft Teams Notification

## Run

```bash
jmeter -n -t jmeter/Smoke-API.jmx -l results/results.jtl -e -o reports
```