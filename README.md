# Playwright Python Tests for Sauce Demo

This project contains automated UI tests for the [Sauce Demo](https://www.saucedemo.com) website using **Playwright** with **Python** and **pytest**.

---

## Project Structure

├── tests/\
│ ├── pages/\
│ │ └── login_page.py # Page Object Model for login page\
│ ├── conftest.py # pytest fixtures for browser, context, and page\
│ └── test_login.py # Test cases for login functionality\
├── requirements.txt # Python dependencies\
└── README.md # This file


## 🛠 Features

- **Page Object Model** for maintainable test code
- **Pytest fixtures** for browser, context, and page management
- **Positive and negative** login test cases
- Easily configurable for **headless/headed mode**

## 📋 Prerequisites

- Python 3.8+
- [pip](https://pip.pypa.io/en/stable/installation/) package manager

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/playwright-ui-test.git
   cd playwright-ui-test

2. Install dependencies:
   pip install pytest playwright

3. Install Playwright browsers:
   playwright install

▶ Running the Tests\
Run all tests:\
pytest

Run tests with a headed browser:\
pytest --headed

Run tests with HTML report:\
pytest --html=report.html --self-contained-html

📂 Example Test Cases\
test_login.py
test_successful_login: Verifies that a valid user can log in and navigate to the inventory page.
test_locked_out_user: Verifies that a locked-out user sees the appropriate error message.

🖥 Sample Code\
login_page.py

from playwright.sync_api import Page

class LoginPage:\
    def __init__(self, page: Page):
        self.page = page
        self.username_input = page.locator("#user-name")
        self.password_input = page.locator("#password")
        self.login_button = page.locator("#login-button")

    def navigate(self):
        self.page.goto("https://www.saucedemo.com/")

    def login(self, username: str, password: str):
        self.username_input.fill(username)
        self.password_input.fill(password)
        self.login_button.click()


📜 License
This project is licensed under the MIT License.