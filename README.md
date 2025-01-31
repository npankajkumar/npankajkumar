- 👋 Hi, I’m @npankajkumar
- 👀 I’m interested in Full Stack | dotnet Development | Java | Python
- 🌱 I’m currently working on FullStack
- 💞️ I’m looking to collaborate on openSource
- 📫 How to reach me npankajkumar0505@gmail.com

<!---
npankajkumar/npankajkumar is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->



# Playwright Testing Guide

Welcome to our **Playwright** test suite! 🚀 This guide will help you set up, write, and run test cases effectively.

---

## 📌 Getting Started

### 1️⃣ Install Dependencies

Before running tests, install all necessary packages:

````sh
npm install


/root-folder
│── playwright.config.ts    # Playwright configuration (baseURL, browser settings, etc.)
│── .gitignore              # Ignoring test artifacts
│── package.json            # Project dependencies
│── .env                    # Store environment variables (e.g., access token)
│── playwright/             # All Playwright-related files live here
│   │── tests/              # Test cases go inside this folder
│   │── pages/              # Page object model (POM) files
│   │── utils/              # Reusable helper functions
│   │── test-results/       # Playwright test results (ignored in Git)
│   │── playwright-report/  # HTML reports (ignored in Git)



### 📝 Writing Test Cases
Navigate to the playwright/pages folder.
Create a separate folder for the page you are testing.
Name your test files as <filename>.spec.ts.
📌 Example:
If testing the Role Setup page, create a test file:


playwright/tests/RoleSetup.spec.ts


# Playwright Testing Guide

Welcome to our **Playwright** test suite! 🚀 This guide will help you set up, write, and run test cases effectively.

---

## 📌 Getting Started

### 1️⃣ Install Dependencies
Before running tests, install all necessary packages:

```sh
npm install
📂 Project Structure

/root-folder
│── playwright.config.ts    # Playwright configuration (baseURL, browser settings, etc.)
│── .gitignore              # Ignoring test artifacts
│── package.json            # Project dependencies
│── .env                    # Store environment variables (e.g., access token)
│── playwright/             # All Playwright-related files live here
│   │── tests/              # Test cases go inside this folder
│   │── pages/              # Page object model (POM) files
│   │── utils/              # Reusable helper functions
│   │── test-results/       # Playwright test results (ignored in Git)
│   │── playwright-report/  # HTML reports (ignored in Git)


📝 Writing Test Cases
Navigate to the playwright/pages folder.
Create a separate folder for the page you are testing.
Name your test files as <filename>.spec.ts.
📌 Example: RoleSetup.spec.ts

If testing the Role Setup table in pricing sheet, create a test file:

playwright/tests/pricing&schedule/RoleSetup.spec.ts



🔑 Environment Variables
Store your ACCESS_TOKEN in the .env file inside the project root.
Example .env file:
env

ACCESS_TOKEN=your_dev_environment_access_token
Access it in your tests using process.env.ACCESS_TOKEN.
🚀 Running Test Cases
Run All Tests


npx playwright test
Run a Specific Test File


npx playwright test <file-path>
📌 Example:



npx playwright test ./playwright/tests/RoleSetup.spec.ts
🔧 Utilities & Code Organization
Use the /playwright/utils/ folder for reusable functions and helper methods.
Keep test files clean and modular.
🛠 VS Code Extensions for Easier Testing
For better productivity, install the Playwright Test for VS Code extension by Microsoft.

👉 Get the Playwright VS Code Extension

🌍 Browser Configuration
By default, Playwright is configured to run in Google Chrome.
If you need to test in other browsers, modify your test file accordingly:


test.use({ browserName: 'firefox' });


💡 Best Practices
✔ Follow the Page Object Model (POM) for better test structure.
✔ Keep reusable functions inside /utils.
✔ Use .env for secrets instead of hardcoding.
✔ Regularly run npx playwright test to validate all tests.

Happy Testing! 🎭🚀
````

