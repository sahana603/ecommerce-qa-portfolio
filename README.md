# E-Commerce Web App — QA Portfolio Project

A complete Quality Assurance portfolio project covering manual testing, UI automation, API testing, and performance testing on a real e-commerce demo application.

---

## Application Under Test

**SauceDemo** — https://www.saucedemo.com  
A publicly available e-commerce demo app built for QA practice.

---

## Tools & Technologies

| Area                | Tool Used              |
|---------------------|------------------------|
| Manual Testing      | Excel / Google Sheets  |
| UI Automation       | Selenium + Python/Java |
| API Testing         | Postman                |
| Performance Testing | Apache JMeter          |
| Version Control     | Git + GitHub           |
| Test Framework      | Pytest / TestNG        |

---

## Project Structure

```
ecommerce-qa-portfolio/
│
├── README.md                  ← You are here
├── TEST_PLAN.md               ← Scope, approach, tools, entry/exit criteria
├── BUG_REPORT.md              ← All bugs found during testing
│
├── manual-tests/
│   └── test-cases.xlsx        ← 30 test cases across login, cart, checkout
│
├── automation/
│   ├── pages/                 ← Page Object Model classes
│   └── tests/                 ← Selenium test scripts
│
├── api-tests/
│   └── saucedemo-api.postman_collection.json
│
└── performance-tests/
    └── load-test-login.jmx    ← JMeter test plan
```

---

## What Was Tested

### Manual Testing
- User login (valid and invalid credentials)
- Product listing and sorting
- Add to cart / remove from cart
- Checkout flow (complete and incomplete)
- Logout functionality

### UI Automation (Selenium)
- Login with valid credentials
- Login with invalid credentials
- Add product to cart and verify cart count
- Complete end-to-end checkout
- Verify product sort order

### API Testing (Postman)
- GET products endpoint
- POST login / authentication
- Validate response status codes and body schema
- Negative test: invalid token / missing fields

### Performance Testing (JMeter)
- 10 virtual users hitting the login endpoint
- Measured: response time, throughput, error rate

---

## Key Findings

- Found **X bugs** during manual testing (see BUG_REPORT.md)
- Automated **8 test scenarios** using Selenium with Page Object Model
- Average login API response time under 10 concurrent users: **~Xms**

---

## How to Run Automation Tests

```bash
# Clone the repo
git clone https://github.com/sahana603/ecommerce-qa-portfolio.git

# Install dependencies (Python)
pip install selenium pytest

# Run tests
pytest automation/tests/
```

---

## About

This project was built to demonstrate real-world QA skills including test planning, manual test case writing, automation scripting, API validation, and performance testing.

**Connect with me on LinkedIn:** www.linkedin.com/in/sahana-fathima-anvar-62ba32291

