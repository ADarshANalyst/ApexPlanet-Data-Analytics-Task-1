ApexPlanet Data Analytics Internship --- Task 1

## Data Immersion & Wrangling

### Project Overview

This project focuses on understanding, profiling, and preparing a sales
dataset for analysis as part of Task 1 of the ApexPlanet Data Analytics
Internship.

The objective is to understand the structure and quality of the data,
document its fields, identify data-quality issues, and prepare a
reliable cleaned dataset for further analysis.

### Dataset Overview

-   **Source file:** `ApexPlanet_DataAnalytics_Dataset.xlsx`
-   **Worksheet:** `Sales_Dataset`
-   **Rows:** 1,000
-   **Columns:** 12
-   **Domain:** Sales and customer orders

### Fields in the Dataset

`Order_ID`, `Order_Date`, `Customer_ID`, `Customer_Name`, `Age`,
`Gender`, `City`, `Product`, `Category`, `Quantity`, `Unit_Price`, and
`Total_Sales`.

### Data Dictionary

The file
[`ApexPlanet_Task1_Data_Dictionary.xlsx`](ApexPlanet_Task1_Data_Dictionary.xlsx)
documents the dataset columns, descriptions, data types, example values,
business relevance, and missing-value counts.

### Initial Data Quality Observations

Initial profiling identified: - 20 missing values in `Age`. - 13 missing
values in `City`. - No fully duplicated rows in the initial dataset.

These observations describe the source dataset before cleaning. Missing
values will be handled carefully, and assumptions will be documented.
Sales totals will be validated against quantity and unit price before
deciding whether any corrections are needed.

### Tools

-   Microsoft Excel --- initial inspection and data dictionary
-   Python --- data profiling and cleaning
-   Pandas --- dataset manipulation and validation
-   OpenPyXL --- reading Excel workbooks

### Planned Workflow

1.  Inspect the source dataset and understand each field.
2.  Profile missing values, duplicates, data types, and inconsistent
    formatting.
3.  Apply justified cleaning steps without silently changing valid data.
4.  Validate key fields and sales calculations.
5.  Export the cleaned dataset as `cleaned_sales_dataset.csv`.
6.  Document the workflow and results.

### Repository Files

  -----------------------------------------------------------------------------
  File                                      Purpose
  ----------------------------------------- -----------------------------------
  `README.md`                               Project overview, workflow, and
                                            documentation

  `ApexPlanet_Task1_Data_Dictionary.xlsx`   Data dictionary and initial
                                            data-quality notes

  `ApexPlanet_DataAnalytics_Dataset.xlsx`   Original dataset, only if sharing
                                            is permitted

  `data_cleaning.py`                        Python cleaning script (to be
                                            added)

  `cleaned_sales_dataset.csv`               Cleaned output (to be added)
  -----------------------------------------------------------------------------

### Status

-   [x] Repository created
-   [x] Data dictionary prepared and uploaded
-   [x] Data-cleaning script completed and uploaded
-   [ ] Cleaned dataset generated and uploaded
-   [ ] Final cleaning results documented

### Notes

-   Upload the original dataset to a public repository only if
    internship data-sharing rules permit it.
-   Do not publish confidential or personally identifiable information.
-   Update this README after the cleaning script is run so the final
    results accurately reflect the actual cleaning performed.

------------------------------------------------------------------------

**Project:** ApexPlanet Data Analytics Internship --- Task 1\
**Focus:** Data Immersion & Wrangling
