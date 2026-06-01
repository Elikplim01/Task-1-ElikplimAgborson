
# Project 1: Data Cleaning & Preparation

## Objective
Formulated a pristine data foundation from a raw transaction ledger containing 1,200 records. Prioritized data integrity over visualization to establish a reliable source of truth.

## Transformations & Quality Checks
* **Standardized Date Formats:** Converted the `Transaction_Date` column from mixed text formats into a uniform Short Date (`DD-MM-YYYY`) format to ensure proper timeline intelligence.

* **Trimmed Category Whitespace:** Applied the `TRIM` function to the `Product_Category` column, stripping out leading/trailing spaces to eliminate duplicate categorical entities.

* **Corrected Identification Columns:** Explicitly cast `Transaction_ID` and `Customer_ID` as Text fields, preventing Excel from corrupting long IDs into scientific notation (`4.5E+11`).

* **Enforced Numeric Typing:** Explicitly cast `Quantity_Purchased` as whole numbers, and both `Price_Per_Unit` and `Total_Amount` as Currency decimal values.

* **Validated Mathematical Integrity:** Generated an audit column calculating `Quantity_Purchased * Price_Per_Unit` across all rows, checking for rounding discrepancies against the existing revenue metric.

