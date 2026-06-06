# Test Plan — E-Commerce Web App (SauceDemo)

## 1. Introduction
This test plan outlines the testing strategy, scope, tools, and schedule for the QA portfolio project on SauceDemo (https://www.saucedemo.com), a publicly available e-commerce demo application.

---

## 2. Objectives
- Validate that core user flows work as expected
- Identify and document bugs and defects
- Automate critical test scenarios using Selenium with Java
- Validate API endpoints using Postman
- Measure performance under load using JMeter

---

## 3. Scope

### In Scope
- User login and logout
- Product listing, sorting, and filtering
- Add to cart / remove from cart
- Checkout flow (personal info, order summary, order confirmation)
- API endpoints (authentication, products)
- Performance of login endpoint under load

### Out of Scope
- Payment gateway integration (not available on demo app)
- Mobile app testing
- Database-level testing

---

## 4. Test Types

| Test Type           | Description                                      | Tool Used              |
|---------------------|--------------------------------------------------|------------------------|
| Manual Testing      | Execute test cases manually and log results      | Excel / Google Sheets  |
| UI Automation       | Automate critical user flows via browser         | Selenium + Java + TestNG |
| API Testing         | Validate REST API endpoints                      | Postman                |
| Performance Testing | Load test login endpoint with virtual users      | Apache JMeter          |

---

## 5. Test Environment

| Component     | Details                          |
|---------------|----------------------------------|
| Application   | https://www.saucedemo.com        |
| Browser       | Google Chrome (latest)           |
| OS            | Windows 10/11                    |
| Language      | Java (JDK 11 or above)           |
| Framework     | TestNG                           |
| Build Tool    | Maven                            |
| IDE           | IntelliJ IDEA / Eclipse          |

---

## 6. Test Credentials

| Username                | Password     | Expected Behavior          |
|-------------------------|--------------|----------------------------|
| standard_user           | secret_sauce | Successful login           |
| locked_out_user         | secret_sauce | Login blocked (error msg)  |
| problem_user            | secret_sauce | Login works, UI has bugs   |
| performance_glitch_user | secret_sauce | Login works but slow       |

---

## 7. Entry Criteria
- Application is accessible at the URL
- Test cases are written and reviewed
- JDK, Maven, and IntelliJ IDEA are installed and configured
- GitHub repo is set up

## 8. Exit Criteria
- All planned test cases have been executed
- All bugs have been logged in BUG_REPORT.md
- Automation scripts are committed to GitHub
- Postman collection is exported and committed
- JMeter results are saved and committed

---

## 9. Deliverables
- `manual-tests/test-cases.xlsx` — all manual test cases
- `BUG_REPORT.md` — all bugs found
- `automation/tests/` — Selenium + Java + TestNG scripts
- `automation/pages/` — Page Object Model classes
- `api-tests/` — Postman collection
- `performance-tests/` — JMeter test plan and results

---

## 10. Schedule

| Phase   | Activity                          | Duration  |
|---------|-----------------------------------|-----------|
| Phase 1 | Project setup & planning          | 2 days    |
| Phase 2 | Test plan & manual test cases     | 2 days    |
| Phase 3 | Manual test execution             | 2 days    |
| Phase 4 | Selenium + Java automation        | 5 days    |
| Phase 5 | API testing with Postman          | 2 days    |
| Phase 6 | Performance testing with JMeter   | 2 days    |
| Phase 7 | Documentation & LinkedIn post     | 1 day     |

---

## 11. Risks & Mitigations

| Risk                              | Mitigation                                        |
|-----------------------------------|---------------------------------------------------|
| Demo site goes down               | Take screenshots of test results                  |
| ChromeDriver version mismatch     | Use WebDriverManager Java library (io.github.bonigarcia) |
| Limited API documentation         | Intercept requests via browser DevTools           |
| Maven dependency conflicts        | Lock dependency versions in pom.xml               |

---

## 12. Tools & Dependencies (Maven pom.xml)

```xml
<!-- Selenium -->
<dependency>
    <groupId>org.seleniumhq.selenium</groupId>
    <artifactId>selenium-java</artifactId>
    <version>4.18.1</version>
</dependency>

<!-- TestNG -->
<dependency>
    <groupId>org.testng</groupId>
    <artifactId>testng</artifactId>
    <version>7.9.0</version>
    <scope>test</scope>
</dependency>

<!-- WebDriverManager -->
<dependency>
    <groupId>io.github.bonigarcia</groupId>
    <artifactId>webdrivermanager</artifactId>
    <version>5.7.0</version>
</dependency>
```

---

## 13. How to Run Automation Tests

```bash
# Clone the repo
git clone https://github.com/sahana603/ecommerce-qa-portfolio.git

# Navigate to automation folder
cd ecommerce-qa-portfolio/automation

# Run all tests using Maven
mvn test
```

---

*Prepared by: Sahana Fathima*
*Project: ecommerce-qa-portfolio*
*GitHub: https://github.com/sahana603/ecommerce-qa-portfolio*
