# Personal Amazon Order History — Exploratory Data Analysis

## Overview
This notebook explores an Amazon order-history spreadsheet with pandas. Although the original notebook called this a “commercial store” analysis, its columns and saved examples look like an individual order-history export, so this README describes it as **personal order-history analysis**, not retail-company sales analytics.

## Notebook
- [Open the analysis notebook](./sale%20data%20analysis%20of%20commercial%20store%20Amazon.ipynb)

## Analysis already present in the notebook
The notebook includes:
- Initial inspection of the table and its dimensions
- Missing-value handling and column removal
- Order totals, mean/median, minimum/maximum, and tax calculations
- Monthly totals, payment-instrument counts, and order-status counts
- Charts for order amounts, cumulative spending, tax, and shipping

The notebook's **saved outputs** show 59 rows and 23 original columns, with order dates from April through July 2019. Its saved output also reports total charged of $1,777.73 and average order value of $30.13. These are historical notebook outputs, not independently rerun or validated results; rerun the analysis against the intended source file before relying on them.

## Local setup

```bash
python -m venv .venv
# Activate the virtual environment for your operating system, then:
python -m pip install -r requirements.txt
jupyter notebook
```

The CSV/XLSX inputs noted below are not included, so supply a permitted dataset and update the notebook input path before running all cells.

## Reproducibility limitation
The notebook reads from a Windows-local file path (`D:\\amazon_orders.xlsx`). That file is not included here, so a clean checkout cannot reproduce the notebook as-is. Update the input path or add a properly licensed, anonymized sample dataset before rerunning.

## Data-quality improvements to make
1. Check missing values column by column before filling them. Replacing all missing values with `0` can corrupt dates, categories, and financial fields.
2. Validate date parsing, numeric types, order-ID uniqueness, and arithmetic consistency between subtotal, tax, promotions, shipping, and total.
3. Aggregate by month using a datetime or period column and label the reporting currency explicitly.
4. Remove or mask names, emails, addresses, order identifiers, and any identifying notebook outputs before making the repository public.
5. Restart the kernel and run every cell in order after fixing the input path.

## Tools
Python, pandas, Jupyter Notebook, Matplotlib, and Seaborn (as used in the notebook).

## Scope
This is exploratory analysis of a small personal order-history export, not evidence of commercial-store performance. No business recommendations should be drawn until the input data and calculations have been reviewed.
