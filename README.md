# JobbyApp E2E Test Cases

This repository contains the automated end-to-end (E2E) test cases for the JobbyApp application. The tests have been implemented based on my knowledge and expertise in Selenium, TestNG, and Java. The following sections detail the setup, structure, and execution of the test cases, along with their results.

---

## Application Details
**Application URL:** [JobbyApp Login Page](https://qajobbyapp.ccbp.tech/login)

---

## Project Structure

The project follows a modular structure, with the following directories and files:

- **`src/test/java/pages`**: Contains page classes implemented using the Page Factory design pattern.
    - `LoginPage.java`
    - `HomePage.java`
    - `HeaderSection.java`
    - `JobsPage.java`
- **`src/test/java`**: Contains test classes for the respective pages.
    - `LoginPageTest.java`
    - `HomePageTest.java`
    - `HeaderSectionTest.java`
    - `JobsPageTest.java`
- **`testng.xml`**: TestNG configuration file for running the tests.

---

## Setup Instructions

### Prerequisites
- Java Development Kit (JDK 8+)
- Maven
- Selenium WebDriver
- TestNG

### Steps to Set Up
1. Clone this repository:
   ```bash
   git clone https://github.com/Aravindh9490/selenium-project-for-jobbly-app-at-E2E-test-cases-.git
   ```
2. Navigate to the project directory:
   ```bash
   cd selenium-project-for-jobbly-app-at-E2E-test-cases-
   ```
3. Install dependencies:
   ```bash
   mvn install
   ```
4. Run the tests:
   ```bash
   mvn test
   ```

---

## Test Cases Overview

### Login Page
#### Test Scenarios
1. **UI Validation**
   - Verifies the presence of UI elements such as the app logo and labels.
   - Validates that the `USERNAME` and `PASSWORD` labels match the expected text.
2. **Form Submission**
   - Handles various submission cases:
     - Empty input fields
     - Empty Username or Password fields
     - Invalid credentials
     - Successful login

#### Results
| Test Scenario                             | Status   | Notes                                   |
|------------------------------------------|----------|-----------------------------------------|
| UI Validation                            | Passed   | All elements displayed correctly.       |
| Submission with empty fields             | Passed   | Error message displayed as expected.    |
| Submission with empty Username field     | Passed   | Error message displayed as expected.    |
| Submission with empty Password field     | Passed   | Error message displayed as expected.    |
| Submission with invalid credentials      | Passed   | Error message displayed as expected.    |
| Successful Login                         | Passed   | Navigated to Home Page successfully.    |

### Home Page
#### Test Scenarios
1. **UI Validation**
   - Validates the heading and description text.
   - Tests the functionality of the "Find Jobs" button.

#### Results
| Test Scenario                 | Status   | Notes                                   |
|-------------------------------|----------|-----------------------------------------|
| Validate Heading and Text     | Passed   | Text matched expected values.          |
| "Find Jobs" Button Functionality | Passed   | Navigated to Jobs Page successfully.    |

### Header Section
#### Test Scenarios
1. **Navigation Links**
   - Tests navigation via Navbar links and App logo link.
2. **Logout Functionality**
   - Verifies successful logout and redirection to the login page.

#### Results
| Test Scenario                         | Status   | Notes                                   |
|---------------------------------------|----------|-----------------------------------------|
| App Logo Navigation                   | Passed   | Navigated to Home Page successfully.    |
| Navbar Home Link Navigation           | Passed   | Navigated to Home Page successfully.    |
| Navbar Jobs Link Navigation           | Passed   | Navigated to Jobs Page successfully.    |
| Logout Functionality                  | Passed   | Logged out and navigated to Login Page. |

### Jobs Page
#### Test Scenarios
1. **Profile Container**
   - Validates UI elements such as profile image, name, and bio text.
2. **Search Functionality**
   - Tests both successful and unsuccessful searches.

#### Results
| Test Scenario               | Status   | Notes                                   |
|-----------------------------|----------|-----------------------------------------|
| Profile Container Validation| Passed   | All elements displayed correctly.       |
| Successful Search           | Passed   | Jobs count matched expected values.     |
| Unsuccessful Search         | Passed   | "No Jobs Found" message displayed.      |

---

## Parallel Testing
Parallel testing was implemented using the `parallel` attribute in the TestNG configuration file, with a specified thread count for efficient execution.

---

## Conclusion
This project demonstrates the implementation of robust E2E tests for the JobbyApp application, ensuring the application's functionality and UI elements perform as expected. The results indicate that all scenarios passed successfully.
