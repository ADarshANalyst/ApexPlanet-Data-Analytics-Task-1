# 📊 Sales Data Wrangling and Cleaning Project

**Task 1 | Data Analytics Project | Python, Pandas & NumPy**

## 📌 Project Overviews

Data wrangling is the process of collecting, cleaning, transforming, and validating raw data to make it suitable for analysis.

This project focuses on cleaning and validating a sample sales dataset containing **1,000 records**. The dataset includes order information, customer details, product categories, quantities, unit prices, and total sales.

The project was implemented using Python in Google Colab, with Pandas and NumPy for data manipulation and analysis.

The primary goal is to improve data quality, handle missing values, identify duplicate records, validate sales calculations, and prepare a cleaned dataset for further analysis.

## 🎯 Project Objectives

- Load and inspect an Excel sales dataset using Python.
- Identify and handle missing values.
- Detect exact duplicate rows.
- Identify repeated order IDs and flag them for review.
- Validate numeric columns and date formats.
- Verify sales calculations using quantity and unit price.
- Generate a data quality report.
- Export the cleaned dataset into CSV and Excel formats.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data cleaning and processing |
| Pandas | Data manipulation and validation |
| NumPy | Numerical operations |
| Google Colab | Cloud-based Python environment |
| Excel | Source dataset |
| GitHub | Project version control and portfolio |

## 📁 Dataset Description

The dataset contains 1,000 rows of sample sales records.

### Dataset Columns

| Column | Description |
|---|---|
| `Order_ID` | Unique order reference expected by the dataset design |
| `Order_Date` | Date associated with the order |
| `Customer_ID` | Customer identifier |
| `Customer_Name` | Customer name or sample label |
| `Age` | Customer age |
| `Gender` | Customer gender |
| `City` | Customer city |
| `Product` | Product purchased |
| `Category` | Product category |
| `Quantity` | Number of units purchased |
| `Unit_Price` | Price per unit |
| `Total_Sales` | Total sales amount for the record |

The cleaned dataset also contains `Duplicate_Order_ID_Flag`, a Boolean column used to identify rows associated with repeated order IDs.

## 🔄 Data Wrangling Workflow

### 1. Data Loading

The original Excel file was loaded into a Pandas DataFrame using `pd.read_excel()`.

### 2. Data Inspection

The dataset was inspected to understand:

- Number of rows and columns.
- Column names and data types.
- Missing values.
- Duplicate records.
- Numeric fields and date formats.

### 3. Missing Value Treatment

**Age**

- Identified 20 missing age values.
- Filled missing ages using the median of available age values.
- Preserved the records rather than deleting entire rows.

**City**

- Identified 13 missing city values.
- Replaced missing city values with `Unknown`.
- Preserved the affected records for future analysis.

These operations impute missing values; they do not recover the original unknown values.

### 4. Duplicate Record Detection

Exact duplicate rows were checked using Pandas duplicate-detection methods.

**Result:** No exact duplicate rows were detected.

### 5. Repeated Order ID Investigation

The `Order_ID` column was checked for repeated values.

The ID `ORD100050` appeared in nine rows and was associated with nine distinct customers and nine distinct order dates.

Since the dataset is sample data, these records were flagged rather than deleted or automatically corrected. The repeated ID should be investigated if the dataset is expected to have one order ID per customer and order date.

### 6. Sales Calculation Validation

The following relationship was used to validate the sales values:

`Expected Total Sales = Quantity × Unit_Price`

The calculated sales values were compared with the existing `Total_Sales` column using a tolerance of `0.01` to allow for minor floating-point or rounding differences.

**Result:** Zero sales calculation mismatches were detected.

### 7. Data Export

The cleaned dataset and data quality report were prepared for export into CSV and Excel formats.

## 📈 Final Data Quality Results

| Quality Check | Result |
|---|---:|
| Total records | 1,000 |
| Columns, including quality flag | 13 |
| Missing values after cleaning | 0 |
| Exact duplicate rows | 0 |
| Rows flagged for repeated Order IDs | 9 |
| Sales calculation mismatches | 0 |

### Key Findings

- All missing values were handled according to the project's cleaning rules.
- No exact duplicate rows remained.
- Sales calculations matched within the defined tolerance.
- Nine rows associated with a repeated order ID were flagged for review rather than removed.
- The cleaned dataset is ready for further exploratory data analysis, subject to the repeated-ID investigation and any additional business rules.

## 📂 Project Structure

The intended repository structure is:

```text
Data-Wrangling-Project/
│
├── README.md
├── Data_Wrangling_Project.ipynb
├── cleaned_sales_dataset.csv
├── cleaned_sales_dataset.xlsx
└── data_quality_report.csv
```

**Files:**

- `README.md` — Project documentation.
- `Data_Wrangling_Project.ipynb` — Python code, cleaning steps, and validation results.
- `cleaned_sales_dataset.csv` — Cleaned dataset in CSV format.
- `cleaned_sales_dataset.xlsx` — Cleaned dataset in Excel format.
- `data_quality_report.csv` — Summary of data quality checks.

*Note: This structure describes the intended deliverables. Include each file in the repository after generating and verifying it.*

## ▶️ How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Open `Data_Wrangling_Project.ipynb`, or upload the notebook if it is stored locally.
3. Upload the original Excel dataset when prompted.
4. Run the notebook cells in sequence.
5. Review the data quality checks and validation results.
6. Generate and download the cleaned dataset and report files.

### Option 2: Run Locally

Install the required libraries:

```bash
pip install pandas numpy openpyxl jupyter
```

Open the notebook:

```bash
jupyter notebook
```

Select `Data_Wrangling_Project.ipynb` and run its cells in sequence. Ensure that the original Excel dataset is available at the file path expected by the notebook.

## 💻 Example: Sales Validation Code

The following Python snippet demonstrates the main sales validation check:

```python
expected_sales = (
    clean_df["Quantity"] * clean_df["Unit_Price"]
)

sales_mismatch = (
    clean_df["Total_Sales"] - expected_sales
).abs() > 0.01

print("Sales mismatches:", sales_mismatch.sum())
```

Expected result for this dataset:

```text
Sales mismatches: 0
```

## ⚠️ Limitations and Considerations

- The dataset contains sample data and may not represent real-world sales patterns.
- Median imputation changes missing age entries to an estimated value; the original ages remain unknown.
- `Unknown` indicates missing city information, not a verified city.
- A repeated order ID does not automatically prove that records are duplicates.
- The repeated `ORD100050` records were flagged, not deleted. Their correctness depends on the intended data model.
- Validation results depend on the rules and assumptions applied during cleaning.

## 🚀 Future Improvements

Potential improvements include:

- Exploratory Data Analysis (EDA).
- Monthly and yearly sales trend analysis.
- Revenue analysis by city and product category.
- Customer segmentation.
- Outlier detection.
- Automated data quality checks.
- Interactive dashboards using Power BI or Tableau.

## 📚 Skills Demonstrated

- Data cleaning and preprocessing.
- Missing value handling.
- Duplicate detection.
- Data type validation.
- Data integrity checks.
- Numerical validation using Pandas and NumPy.
- Excel and CSV data processing.
- Python programming in Google Colab.
- GitHub project documentation.

## 👨‍💻 Author

**Adarsh Porwal**

Data Analytics Learner | Python | Pandas | NumPy | Data Wrangling

GitHub: https://github.com/ADarshANalyst

## 📄 License

This project is intended for educational and portfolio purposes. Add an appropriate license if you plan to distribute or reuse the project publicly.

---

**Project Status:** Data cleaning and validation completed; repeated order ID flagged for review.

**Thank you for visiting this project!**
