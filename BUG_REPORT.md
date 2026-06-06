# Bug Report — E-Commerce Web App (SauceDemo)

## How to Read This Report

| Column       | Description                                                  |
|--------------|--------------------------------------------------------------|
| Bug ID       | Unique identifier for the bug                                |
| Title        | Short description of the issue                               |
| Severity     | Critical / High / Medium / Low                               |
| Priority     | P1 (fix immediately) to P4 (fix later)                       |
| Status       | Open / In Progress / Fixed / Closed                          |
| Steps        | How to reproduce the bug                                     |
| Expected     | What should happen                                           |
| Actual       | What actually happened                                       |

---

## Severity Definitions

- **Critical** — App crashes or core feature is completely broken
- **High** — Major feature broken but workaround exists
- **Medium** — Feature works but with incorrect behavior
- **Low** — Minor UI or cosmetic issue

---

## Bug Log

---

### BUG-001
**Title:** Locked out user sees no helpful error message  
**Severity:** High  
**Priority:** P2  
**Status:** Open  
**Module:** Login  

**Steps to Reproduce:**
1. Go to https://www.saucedemo.com
2. Enter username: `locked_out_user`
3. Enter password: `secret_sauce`
4. Click Login

**Expected Result:** A clear message like "Your account has been locked. Please contact support."  
**Actual Result:** Generic error message shown — not user-friendly  
**Screenshot:** *(attach screenshot here)*

---

### BUG-002
**Title:** Problem user product images are broken/incorrect  
**Severity:** Medium  
**Priority:** P3  
**Status:** Open  
**Module:** Product Listing  

**Steps to Reproduce:**
1. Login with username: `problem_user`, password: `secret_sauce`
2. View the product listing page

**Expected Result:** All product images should display correctly  
**Actual Result:** All product images show the same wrong image  
**Screenshot:** *(attach screenshot here)*

---

### BUG-003
**Title:** Performance glitch user experiences extreme login delay  
**Severity:** Medium  
**Priority:** P3  
**Status:** Open  
**Module:** Login / Performance  

**Steps to Reproduce:**
1. Login with username: `performance_glitch_user`, password: `secret_sauce`
2. Observe login time

**Expected Result:** Login should complete within 2-3 seconds  
**Actual Result:** Login takes 5+ seconds — poor user experience  
**Screenshot:** *(attach screenshot here)*

---

## Template for New Bugs

Copy and use this template when you find new bugs during testing:

```
### BUG-00X
**Title:**  
**Severity:**  
**Priority:**  
**Status:** Open  
**Module:**  

**Steps to Reproduce:**
1. 
2. 
3. 

**Expected Result:**  
**Actual Result:**  
**Screenshot:** *(attach here)*
```

---

*Project: ecommerce-qa-portfolio*  
*Tester: Sahana Fathima*  
*GitHub: https://github.com/sahana603/ecommerce-qa-portfolio*
