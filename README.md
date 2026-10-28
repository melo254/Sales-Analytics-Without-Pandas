# Tech Hub Kenya - Sales Analytics

## Project Overview

This project analyzes Tech Hub Kenya's September 2026 electronics sales data using Python's standard library, with pandas used to verify the results.

The analysis focuses on revenue performance, product and store comparisons, payment methods, high-value transactions, and data quality.

## Dataset

- **Period:** September 2026
- **Original transactions:** 50
- **Clean transactions:** 45
- **Skipped transactions:** 5
- **Currency:** Kenyan Shillings (KES)

The dataset contains transaction dates, stores, products, quantities, unit prices, and payment methods.

## Tools and Technologies

- Python
- CSV module
- `pathlib`
- pandas
- Jupyter Notebook

## Analysis Performed

1. Loaded raw sales records from a CSV file.
2. Cleaned and validated numeric quantities and unit prices.
3. Calculated revenue for each valid transaction.
4. Calculated total revenue and revenue by product, store, and payment method.
5. Identified the top three products by revenue.
6. Identified high-value transactions exceeding KES 50,000.
7. Calculated mean, median, minimum, and maximum transaction revenue.
8. Verified the main results using pandas.

## Key Findings

- **Total revenue:** KES 1,291,813.00 across 45 valid transactions.
- **Top-performing product:** HP 15 Laptop, generating KES 389,994.00.
- **Top-performing store:** Kisumu Mega Plaza, generating KES 449,678.00.
- **Leading payment method:** M-Pesa, accounting for KES 738,568.00 in revenue.
- **High-value transactions:** Five transactions exceeded KES 50,000.

## Data Cleaning

Transactions with missing or invalid quantities or unit prices were skipped. Transactions with zero or negative quantities or unit prices were also excluded.

The `parse_number()` function validates numeric values, including comma-separated thousands, before calculations are performed.

## Project Structure

```text
day2-sales-analytics/
├── sales_analysis.ipynb
├── data/
│   └── electronics_sales.csv
├── output/
│   └── sales_report.txt
├── requirements.txt
└── README.md
```

## How to Run

1. Clone or download the repository.
2. Create and activate a Python virtual environment.
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open `sales_analysis.ipynb` in VS Code or Jupyter Notebook.
5. Run the notebook cells in order.
6. Review the generated report at `output/sales_report.txt`.

## Verification

The notebook recomputes key results with pandas and compares them with the standard-library implementation. All 12 verification checks returned `MATCH`.

**Note:** Both implementations use the same numeric parsing function, so the verification independently checks the calculations and aggregations, not the parsing logic itself.

## Learning Objective

This project demonstrates CSV processing, data cleaning, functions, dictionaries, list comprehensions, sorting, descriptive statistics, file handling, and basic data verification in Python.
