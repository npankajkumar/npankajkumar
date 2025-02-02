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

```sh
npm install
```

📂 Project Structure

```sh

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

-ideal
root/
├── playwright.config.ts
├── tests/
│   ├── setup/
│   │   ├── beforeAll.ts
│   │   ├── beforeEach.ts
│   │   ├── afterEach.ts
│   │   └── afterAll.ts
│   ├── pages/
│   │   ├── loginPage.ts
│   │   ├── dashboardPage.ts
│   │   └── userProfilePage.ts
│   ├── utils/
│   │   ├── customFunctions.ts
│   │   ├── constants.ts
│   │   └── selectors.ts
│   ├── workflows/
│   │   ├── userWorkflow.ts
│   │   └── adminWorkflow.ts
│   ├── api/
│   │   ├── userApi.ts
│   │   └── adminApi.ts
│   └── test/
│       ├── login.spec.ts
│       ├── dashboard.spec.ts
│       └── userProfile.spec.ts
├── package.json
└── package-lock.json

```

## 📝 Writing Test Cases

Navigate to the playwright/pages folder.
Create a separate folder for the page you are testing.

Name your test files as

```javascript
<filename>.spec.ts.

Example: RoleSetup.spec.ts
```

If testing the Role Setup table in pricing sheet, create a test file:

```sh
playwright/tests/pricing&schedule/RoleSetup.spec.ts
```

## 🔑 Environment Variables

Store your ACCESS_TOKEN in the .env file inside the project root.
Example .env file:

```javascript
ACCESS_TOKEN = your_dev_environment_access_token
```

# Access it in your tests using ## process.env.ACCESS_TOKEN.

# 🚀 Running Test Cases

```sh
Run All Tests

# npx playwright test

Run a Specific Test File

# npx playwright test <file-path>


Example:
#npx playwright test ./playwright/tests/RoleSetup.spec.ts

```

## 🔧 Utilities & Code Organization

Use the /playwright/utils/ folder for reusable functions and helper methods.
Keep test files clean and modular.

🛠 VS Code Extensions for Easier Testing
For better productivity, install the Playwright Test for VS Code extension by Microsoft.

## [👉 Get the Playwright VS Code Extension](https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright)

## 🌍 Browser Configuration

By default, Playwright is configured to run in Google Chrome.
If you need to test in other browsers, modify your test file accordingly:

```sh
test.use({ browserName: 'firefox' });
```

## 💡 Best Practices

1. Keep reusable functions inside /utils.
2. Use .env for secrets instead of hardcoding.
3. Regularly run npx playwright test to validate all tests.

# [🎭 Learn playwright](https://allegisgroup.udemy.com/course/playwright-tutorials-automation-testing)

```sh
Happy Testing! 🎭🚀
```
