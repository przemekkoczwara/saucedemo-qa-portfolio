# Test Plan — SauceDemo Manual Testing Project

**Version:** 1.0
**Author:** Przemysław Koczwara
**Date:** 2026-03-31
**Status:** Active

---

## 1. Project Overview

**Application Under Test:** SauceDemo
**URL:** https://www.saucedemo.com
**Type:** Web application — e-commerce demo

SauceDemo is a demo e-commerce application created by Sauce Labs,
designed specifically for practicing manual and automated testing.
It simulates a real online shop with login, product catalog,
shopping cart, and checkout functionality.

**Purpose of this test project:**
To perform comprehensive manual testing of SauceDemo and document
the process as a QA portfolio project, demonstrating ability to
plan, execute, and report software testing activities.

---

## 2. Scope

### In Scope ✅
| Module | What will be tested |
|--------|-------------------|
| Login | Authentication, error messages, all 6 user types |
| Product Catalog | Display, sorting, product details, add to cart |
| Shopping Cart | Add/remove items, cart counter, navigation |
| Checkout | Form validation, order summary, purchase completion |

### Out of Scope ❌
| Area | Reason |
|------|--------|
| Performance testing | Requires dedicated tools (JMeter, k6) |
| Security testing | Beyond manual testing scope |
| Mobile / responsive | Focus on desktop browser only |
| API testing | No API access available for this demo |
| Cross-browser testing | Primary browser: Chrome only |

---

## 3. Test Types

| Type | Description | Applied to |
|------|-------------|------------|
| **Smoke Testing** | Quick check — does the app launch and core functions work? Runs first, before anything else. | Login, navigation, product display |
| **Functional Testing** | Does every feature work according to requirements? Step-by-step verification. | All modules |
| **Negative Testing** | What happens when user makes mistakes? Empty fields, wrong data, unexpected actions. | Login, Checkout forms |
| **Exploratory Testing** | Free-form testing without scripts — tester uses intuition to find unexpected bugs. | problem_user, visual_user |
| **UI Testing** | Does the interface look correct? Correct text, buttons visible, layout not broken. | All modules, visual_user |

---

## 4. Entry and Exit Criteria


### Entry Criteria (when can we START testing?)
- [ ] Application is accessible at https://www.saucedemo.com
- [ ] All 6 test user accounts are working
- [ ] Test cases are written and reviewed
- [ ] JIRA project is set up with Epics and Tasks
- [ ] GitHub repository structure is ready

### Exit Criteria (when can we STOP testing?)
- [ ] 100% of planned test cases executed
- [ ] All Critical and High bugs documented in JIRA
- [ ] Test Run Summary report completed
- [ ] Pass rate ≥ 80% of total test cases
- [ ] No unresolved Critical (blocker) bugs

---

## 5. Test Environment

| Component | Details |
|-----------|---------|
| **Operating System** | macOS 26.3.1 (25D2128) | 
| **Architecture** | Apple Silicon (ARM64) |
| **Primary Browser** | Google Chrome 146.0.7680.165 (Official Build, ARM64) |
| **Screen Resolution** | 15,3'' (2880 × 1864) | 
| **Internet Connection** | Required (online app) |
| **Test Management** | JIRA (Atlassian Free plan) |
| **Documentation** | GitHub (public repository) |
| **Screenshot Tool** | Screenshot (CMD+Shift+4) / CleanShot X |

> Note: Tests are executed manually without test automation tools.
> Hardware: Apple Silicon Mac — ARM64 architecture.

---

## 6. Risks and Mitigations

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| App unavailable (server down) | Low | High | Test during off-peak hours, retry next day |
| Test data reset between sessions | Medium | Medium | Document test data used in each TC |
| Insufficient time to execute all TC | Medium | Medium | Prioritize High priority TC first |
| Unclear expected results | Low | Medium | Base expected results on standard UX patterns |

---

## 7. Timeline (5-Day Sprint)

| Day | Activity | Deliverable |
|-----|----------|-------------|
| Day 1 | Setup JIRA + GitHub, write Test Plan | test-plan.md committed |
| Day 2 | Write Test Cases — Login + Inventory | TC-LOGIN.md, TC-INVENTORY.md |
| Day 3 | Write Test Cases — Cart + Checkout | TC-CART.md, TC-CHECKOUT.md |
| Day 4 | Execute all test cases, document bugs | Bug reports in JIRA + GitHub |
| Day 5 | Write Test Run Summary, finalize README | Portfolio ready to share |

---

## 8. Success Metrics

| Metric | Target |
|--------|--------|
| Total Test Cases written | ≥ 36 |
| Test Case execution rate | 100% |
| Pass rate | ≥ 80% |
| Bugs documented (total) | ≥ 8 |
| Critical bugs documented | All found |
| Bug reports with screenshots | 100% |
