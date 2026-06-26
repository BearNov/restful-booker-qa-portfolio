# Software Test Plan — Restful Booker Platform

## 1. Document Information

* **Project:** Restful Booker QA Portfolio
* **Application Under Test:** Restful Booker Platform
* **Application URL:** https://automationintesting.online/
* **Prepared by:** Baruch Ilhanov
* **Version:** 1.0
* **Status:** Draft

## 2. Purpose

To define the scope, objectives, testing approach, environment, risks, and deliverables for the manual testing of the Restful Booker Platform.

## 3. Test Objectives

To verify that the main customer-facing features work correctly and provide clear feedback to users.

The testing will focus on:

* Navigation
* Room listings and room details
* Availability search
* Booking flow
* Contact form
* Responsive behaviour
* Input validation
* Error handling

## 4. In Scope

This manual web-testing phase covers the main customer-facing features of the Restful Booker Platform:

* Homepage navigation and section links
* Room listings and room-detail pages
* Room information, images, amenities, prices, and guest capacity
* Availability-search date selection and validation
* Booking-date selection and price calculation
* Guest-information form validation
* Successful room reservation flow
* Contact-form validation and successful submission
* User-facing confirmation and error messages
* Basic responsive behaviour at desktop, tablet, and mobile viewport sizes
* Basic cross-browser verification in Firefox and Chrome
* Recording reproducible defects with supporting evidence

## 5. Out of Scope

The following areas are excluded from this manual web-testing phase:

* Administration-panel functionality
* User authentication beyond basic login-page observation
* API testing with Postman
* Direct database testing and SQL validation
* Automated testing
* Performance and load testing
* Penetration testing and advanced security assessment
* Complete accessibility audit
* Testing on every browser, operating system, and physical device
* Email or external notification delivery
* Verification of third-party map data accuracy

API testing and SQL validation will be completed later as separate modules within the overall QA portfolio project.

## 6. Test Approach

Testing will be performed manually from the perspective of a customer using the public web application.

The following testing methods will be used:

* **Functional testing:** Verify that navigation, room browsing, availability search, booking, and contact features behave as expected.
* **Exploratory testing:** Investigate the application to identify unclear behaviour, unexpected results, and potential defects outside predefined test cases.
* **Positive testing:** Use valid dates and valid user information to confirm that successful workflows can be completed.
* **Negative testing:** Use empty, invalid, and incorrectly formatted inputs to verify validation and error handling.
* **Boundary-value testing:** Check values near documented limits, including minimum and maximum field lengths and date boundaries.
* **Responsive testing:** Review the application at desktop, tablet, and mobile viewport sizes.
* **Cross-browser testing:** Execute selected critical scenarios in Firefox and Chrome.
* **Regression testing:** Re-run relevant test cases after reproducing or documenting defects to confirm that existing functions remain consistent.

Formal test cases will be created for the main customer-facing workflows. Additional observations discovered during exploratory testing will be documented separately and converted into test cases or defect reports when appropriate.

Each test case will include:

* Test-case identifier
* Feature or module
* Preconditions
* Test data
* Execution steps
* Expected result
* Actual result
* Status
* Evidence or notes

Potential defects will be reproduced before being formally reported. Each confirmed defect will include clear reproduction steps, expected and actual results, severity, priority, environment details, and supporting screenshots when available.

## 7. Test Environment and Tools

### Test Environment

* **Operating system:** Windows 10
* **Device type:** Desktop computer
* **Primary browser:** Mozilla Firefox
* **Secondary browser:** Google Chrome for selected cross-browser checks
* **Application environment:** Public shared demonstration environment
* **Application URL:** https://automationintesting.online/

### Responsive Viewports

Responsive testing will be performed using Firefox Responsive Design Mode at:

* **Mobile:** 375 × 667
* **Tablet:** 768 × 1024
* **Device pixel ratio:** 1
* **Browser zoom:** 100%
* **Network throttling:** Disabled

### Testing and Documentation Tools

* **Firefox Developer Tools:** Responsive testing and technical investigation
* **Chrome Developer Tools:** Selected cross-browser and technical checks
* **GitHub:** Project documentation, version history, and defect tracking
* **GitHub Issues:** Formal defect reports
* **Microsoft Excel:** Test cases, execution results, and test-data management
* **Screenshots:** Supporting evidence for observations and defects

The exact browser versions used during formal test execution will be recorded in the test-execution results and defect reports.

## 8. Entry Criteria

Formal test execution may begin when the following conditions are met:

* The application is accessible through the public test URL.
* The manual testing scope and test approach have been defined.
* The required test environment and browsers are available.
* The main customer-facing features are accessible for testing.
* The test checklist and formal test cases have been prepared.
* Required test data, including valid and invalid customer details, has been prepared.
* The folders for test results, screenshots, and defect evidence are available in the project repository.
* Known limitations of the shared demonstration environment have been documented.
* No blocking environment issue prevents the main booking and contact workflows from being tested.

## 9. Exit Criteria

To be completed.

## 10. Risks and Assumptions

To be completed.

## 11. Test Deliverables

To be completed.
