# NetlifyTest - Login Module Testing & Bug Report

**Project Overview**  
This repository contains manual testing documentation and bug reports for the **Login module** of a web application hosted on Netlify.  

The main goal of this testing was to evaluate login functionality, input validation, security, performance, and overall user experience.

## Project Information

| Field                  | Value                     |
|------------------------|---------------------------|
| Project Name           | NetlifyTest               |
| Module Name            | Login                     |
| Release Version        | 1.84.141                  |
| Browser                | Brave                     |
| Designed by            | Ramashis Roy              |
| Executed by            | Noman Ibrahim             |
| Test Designed Date     | 19 December 2025          |
| Test Execution Date    | 01 February 2026          |
| **Total Test Cases**   | **6**                     |
| **Total Bugs**         | **8**                     |
| Tests: Pass / Fail / Pending | 6 / 0 / 0              |
| Bugs: Open / Closed / Pending | 8 / 0 / 0             |

## Test Cases Summary

| ID          | Test Scenario                                  | Priority | Type       | Status | Notes                              |
|-------------|------------------------------------------------|----------|------------|--------|------------------------------------|
| TC-LG-001   | Login with valid email and password            | Medium   | Functional | Pass   | —                                  |
| TC-LG-002   | Email with leading/trailing spaces             | High     | Negative   | Pass   | Proper validation                  |
| TC-LG-003   | Both email & password empty                    | High     | Boundary   | Pass   | Required field validation          |
| TC-LG-004   | Empty email only                               | Medium   | Boundary   | Pass   | —                                  |
| TC-LG-005   | Empty password only                            | Medium   | Boundary   | Pass   | —                                  |
| TC-LG-006   | Login attempt with no internet connection      | High     | Negative   | Pass   | Shows "Failed to fetch" message    |

**All test cases passed successfully.**

## Open Bugs Summary

| Bug ID      | Issue Description                              | Priority | Type       | Status | Notes                                      |
|-------------|------------------------------------------------|----------|------------|--------|--------------------------------------------|
| BUG-LG-001  | Password field accepts only spaces             | High     | Validation | Open   | Serious validation issue                   |
| BUG-LG-002  | No maximum length limit on password field      | High     | Validation | Open   | UI slowdown with very long input           |
| BUG-LG-003  | No maximum length limit on email field         | High     | Validation | Open   | Same as above                              |
| BUG-LG-004  | Weak password (no special characters) accepted | High     | Security   | Open   | Very weak password policy                  |
| BUG-LG-005  | Copy-paste allowed in password field           | Medium   | Security   | Open   | Security best practice violation           |
| BUG-LG-006  | Show/Hide password toggle is missing           | Low      | Usability  | Open   | UX improvement needed                      |
| BUG-LG-007  | Login takes too long / poor feedback           | High     | Performance| Open   | No loading indicator, user confusion       |
| BUG-LG-008  | No loading indicator during login process      | Medium   | UX         | Open   | User unsure if request is processing       |

## Screenshots (Recommended)

You can add screenshots in a `/screenshots` folder and link them like this:


### BUG-LG-001 - Password accepts only spaces
[Password only spaces](https://github.com/ramashis06/netlify-test-case-and-bug-report/blob/7815e892c3342f162782949a234befa47a7ae8db/Screenshot%202025-12-25%20020443.png)

### BUG-LG-006 - Missing show/hide toggle
![No toggle](https://github.com/ramashis06/netlify-test-case-and-bug-report/blob/7815e892c3342f162782949a234befa47a7ae8db/Screenshot%202025-12-25%20020443.png)

```
## Environment & Tools


Browser: Brave
Testing Type: Manual
Documentation: Manual (Excel/Google Sheets)
Automation: Not implemented

## Recommendations for Improvement

Implement minimum & maximum length validation for both email and password fields
Enforce a strong password policy (special characters, numbers, mixed case)
Add show/hide password toggle feature
Display a loading spinner/indicator during login requests
Disable copy-paste in the password field
Improve network error handling (custom message + retry option)

Contribution
Feel free to open issues or submit pull requests for bug fixes, additional test cases, or documentation improvements.

Happy Testing! 🚀
