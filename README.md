# 🚀 API Test Automation with CI/CD

## Overview

This project demonstrates basic API test automation using Postman, executed via Newman, and integrated into a CI/CD pipeline using GitHub Actions.

The goal is to simulate a real-world QA workflow, covering functional, negative, and performance validations.

---

## Test Coverage

The following scenarios are automated:

* GET Users (list and validation)
* POST Login (success)
* POST Login (invalid - negative test)
* POST Create User
* PUT Update User
* DELETE User
* Response Delay Validation

---

## Tech Stack

* **Postman** – API testing and request creation
* **Newman** – CLI runner for Postman collections
* **JavaScript** – Test scripts and assertions
* **GitHub Actions** – CI/CD pipeline automation

---

## Project Structure

```
reqres-api-tests/
├── postman/
│   ├── reqres_collection.json
│   └── reqres_environment.json
├── .github/
│   └── workflows/
│       └── api-tests.yml
└── README.md
```

---

## CI/CD Pipeline

This project uses GitHub Actions to automatically run API tests on every push to the `main` branch.

### Pipeline Steps:

* Checkout repository
* Setup Node.js environment
* Install Newman
* Execute Postman collection

---

## How to Run Locally

### 1. Install Newman

```
npm install -g newman
```

### 2. Run the tests

```
newman run postman/reqres_collection.json -e postman/reqres_environment.json
```

---

## Test Validations

The tests include:

* Status code validation
* Response structure validation
* Data validation (fields, types, values)
* Negative scenarios
* Performance check (response time)

---

## Key Learnings

* API test automation with Postman
* Writing assertions using JavaScript
* Running tests via CLI (Newman)
* CI/CD integration with GitHub Actions
* Debugging pipeline execution issues


---

## Contact

Feel free to connect or reach out:

* LinkedIn: https://www.linkedin.com/in/brunostephanschmitt/
* GitHub: https://github.com/bsschmitt