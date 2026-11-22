# InvestWise – Investment Calculators

A responsive, browser-based investment planning application built with plain HTML, CSS and JavaScript. No backend, database, package installation or build step is required.

## Included calculators

1. **Lump Sum / CAGR Investment Return Calculator** – enter a one-time investment, expected CAGR and number of years to estimate future value, profit and year-wise growth.
2. **CAGR Calculator** – calculate annualized growth from initial value, final value and investment duration.
3. **SIP Calculator** – estimate future value from monthly investments, annual return and duration.
4. **SWP Calculator** – estimate monthly withdrawals, total withdrawals and remaining balance over a selected period.

The previous target planner and scenario comparison tool have been removed.

## Run locally

Open `index.html` in a modern browser. Alternatively, run a local server from this folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Sign in to [GitHub](https://github.com/) and create a new repository named `investment-calculator`.
2. Choose **Public** if you want the site to be accessible to anyone with the URL. (A public repository is the simplest option for GitHub Pages on the standard free plan.)
3. Extract this ZIP and upload the **contents** of the `investment-calculator` folder to the repository root. Ensure `index.html`, `css/`, `js/` and `README.md` are at the top level.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch **main** and folder **/(root)**, then click **Save**.
7. Wait for the Pages deployment to complete. Your website will be available at:

   `https://YOUR_GITHUB_USERNAME.github.io/investment-calculator/`

   Replace `YOUR_GITHUB_USERNAME` with your GitHub username. GitHub will also show the exact published URL in **Settings → Pages**.

### Upload using Git commands (optional)

```bash
git init
git add .
git commit -m "Add InvestWise investment calculators"
git branch -M main
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/investment-calculator.git
git push -u origin main
```

Replace `YOUR_GITHUB_USERNAME` with your GitHub username and use the repository URL shown by GitHub.

### Updating the live website

Whenever you change files, commit and push the updates to the `main` branch. GitHub Pages will publish the updated site automatically.

## Calculation conventions and limitations

- **Lump sum:** `FV = PV × (1 + r)^n`, with annual compounding.
- **CAGR:** `(Final value / Initial value)^(1 / years) - 1`.
- **SIP:** assumes month-end contributions. Annual effective return is converted to an equivalent monthly rate before applying the annuity formula.
- **SWP:** assumes a constant equivalent monthly return is credited first, followed by the month-end withdrawal. If the balance is exhausted, subsequent withdrawals are not counted.

The calculations are illustrations, not forecasts or guaranteed returns. They do not account for taxes, inflation, fund expenses, exit loads or market volatility. This tool is not investment advice.

## Project structure

```text
investment-calculator/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── calculator.js
├── assets/
├── .gitlab-ci.yml
└── README.md
```
