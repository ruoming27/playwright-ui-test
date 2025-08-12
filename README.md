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