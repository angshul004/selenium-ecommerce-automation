# Selenium WebDriver E-Commerce Automation

An end-to-end Python/Selenium project for purchasing a product on the [TutorialsNinja demo store](https://tutorialsninja.com/demo/). It covers login, product search, cart updates and verification, screenshots, alert handling, Excel/JSON test data, and an HTML execution report.

## Demonstration Video link

## Prerequisites

- Python 3.10+
- Google Chrome (ChromeDriver is managed automatically by Selenium Manager)
- A valid TutorialsNinja demo-store account. Create one via **My Account > Register** if needed.

## Setup

Open PowerShell in the root folder that contains both `Capstone Project` and `pytest.ini`.

```powershell
python -m venv myenv
.\myenv\Scripts\Activate.ps1
pip install -r "Capstone Project\requirements.txt"
Copy-Item "Capstone Project\.env.example" "Capstone Project\.env"
```

Edit `Capstone Project/.env` with your account credentials.

## Run

From the parent folder, run:

```powershell
pytest
```

Outputs:

- `Capstone Project/reports/execution_report.html` - self-contained pytest HTML report
- `Capstone Project/screenshots/` - timestamped screenshots for key workflow stages and failures
- `Capstone Project/data/test_data.xlsx` - generated Excel test-data source
- `Capstone Project/.pytest_cache/` - pytest's temporary cache

## Project structure

```
project root/
|- pytest.ini              Launch configuration for `pytest`
|- myenv/                  Python virtual environment
`- Capstone Project/
   |- pages/               Page Object Model classes
   |- tests/               Selenium end-to-end tests
   |- utils/               Configuration, browser, data, and helper utilities
   |- data/                JSON seed and generated Excel test data
   |- reports/             HTML execution report output
   `- screenshots/         Screenshot output
```

## Notes

The demo site is public and can be reset or temporarily unavailable. Credentials are intentionally not committed. The test verifies the cart item name, unit price, line total calculation, and requested quantity before it ends; it does not place an irreversible order. All generated outputs remain inside `Capstone Project`.
