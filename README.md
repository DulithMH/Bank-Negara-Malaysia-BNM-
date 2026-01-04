📈 Gold Price Prediction: A Multi-Factor Quant Strategy
🎯 Overview: This project develops a robust machine learning framework to predict the daily direction of Gold prices ($GC=F$). By integrating technical momentum indicators, intermarket data (US Dollar Index), and NLP-based sentiment analysis, the model achieved an "Honest" Accuracy of 61.32% and a Sharpe Ratio of 2.14.

Key Results: Cumulative Return: 85.5% (Outperforming Buy-and-Hold by >2x).Average CV Accuracy: 57.64% (Verified via Time-Series Cross-Validation).Risk-Adjusted Return: Elite Sharpe Ratio of 2.14.🛠️ The Financial Engineering Pipeline1. Data Transformation & Cleaning. To handle the volatility and non-stationarity of financial time series: Log Returns: Raw prices were transformed into stationarity:$$R_t = \ln\left(\frac{P_t}{P_{t-1}}\right)$$Winsorization: Extreme outliers (e.g., the 2017 anomaly) were clipped at the 1st and 99th percentiles to prevent gradient descent distortion.


2. Feature Engineering (The "Alpha" Drivers)
The model looks beyond price history to understand market context:

Technical Indicators: 14-day RSI and 20-day SMA to capture momentum and mean reversion.

Intermarket Logic: Inclusion of the US Dollar Index (DXY) to exploit the inverse correlation between USD and Gold.

Sentiment Analysis: A custom news scraper using BeautifulSoup and TextBlob to quantify global sentiment.

3. Preventing Data Leakage. A critical component of this project was ensuring temporal integrity. All features were lagged by $t-1$ to ensure the model only uses information available before the market opens.

4. Metric, Model Strategy ,Benchmark (Market)
Total Return,85.5%,~40.2%
Sharpe Ratio,2.14,0.85
Max Drawdown ,Lower than Market, High


Backtest Visualization
The strategy demonstrates consistent alpha generation, particularly during high-volatility regimes where the AI managed to "stay in cash" or dodge major downturns.

# BNM Data Set

Short description: concise one-liner describing what this dataset contains, how it was collected, and the primary intended use.

Badges
- Build / CI: ![CI](https://img.shields.io/badge/ci-github%20actions-blue)
- License (code): ![License: MIT](https://img.shields.io/badge/license-MIT-green)
- Data license: ![CC BY 4.0](https://img.shields.io/badge/data-CC--BY--4.0-blue)
- DOI (when released): badge inserted after release
- Binder / Colab (optional): try notebooks live

Quick links
- Dataset overview — data/README.md
- Data dictionary — data/data_dictionary.md
- Notebooks — notebooks/
- Source code — src/
- Contributing — CONTRIBUTING.md
- License — LICENSE (code) and LICENSE-DATA (data)
- Citation — see CITATION.cff or "How to cite" below

Quickstart (local)
1. Clone repository:
   ```
   git clone https://github.com/DulithMH/BNM-Data-Set-.git
   cd BNM-Data-Set-
   ```
2. Create environment (recommended):
   - Conda:
     ```
     conda env create -f environment.yml
     conda activate bnm
     ```
   - Or pip:
     ```
     python -m venv .venv
     source .venv/bin/activate
     pip install -r requirements.txt
     ```
3. Run tests and notebooks:
   ```
   pytest
   # or run notebooks via nbconvert/papermill, see docs
   ```

Repository structure
- data/ — raw and processed data (small example files; large files tracked via Git LFS or DVC)
- notebooks/ — exploratory and reproducible analysis notebooks
- src/ — python package for reusable code and data processing
- tests/ — unit tests and notebook tests (nbval)
- docs/ — project documentation or site
- .github/ — CI workflows and templates

Data license and citation
- This repository uses a separate data license (LICENSE-DATA). Please check it before reusing the dataset.
- Suggested citation (example):
  DulithMH (2026). BNM Data Set. GitHub. https://doi.org/xxxxxx (replace with DOI after release)

Why these choices
- Separate licenses clarify rights for code vs data.
- Environments and CI ensure reproducible results.
- Moving code to src/ makes testing and reuse straightforward.

Next steps
- (Optional) I can create these files as a PR: README, CONTRIBUTING, CODE_OF_CONDUCT, CI, env, and templates. Tell me the preferred data license (CC BY 4.0 recommended) and whether you want me to set up DVC or Git LFS for large files.



