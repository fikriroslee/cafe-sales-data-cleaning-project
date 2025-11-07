# ☕ Cafe Sales Data Cleaning Project (Excel)

## 📋 Project Overview
This project focuses on cleaning and preparing a cafe's sales dataset (**10,000 rows**) using **Microsoft Excel**. The goal was to improve data quality by correcting inconsistencies, handling missing values, validating prices, and creating new features to support further analysis.

**Dataset Source:** https://www.kaggle.com/datasets/ahmedmohamed2003/cafe-sales-dirty-data-for-cleaning-training?select=dirty_cafe_sales.csv

---

## 🎯 Objectives
- Handle missing, ERROR, and UNKNOWN values across multiple columns
- Handle missing or blank transaction dates
- Validate **Quantity**, **Price Per Unit** and **Total Spent** data
- Engineer new columns such as **Category**, **Transaction Day** and **Transaction Month**
- Summarize data with pivot tables for better insight

---

## 🛠️ Tools & Excel Functions Used
- **Microsoft Excel**
- Functions: `TRIM`, `CLEAN`, `LEN`, `ISBLANK`, `ISNUMBER`, `COUNTIF`, `IF`, `OR`, `NOT`, `SUMIF`, `VALUE`, `TEXT`, `VLOOKUP`
- Features: Filter, Conditional Formatting, Data Validation, Pivot Tables

---

## 🧹 Data Cleaning Steps

1. **Text Standardization**  
   Cleaned item names and text fields using `TRIM`, and `CLEAN` to ensure consistent formatting. 

2. **Data Validation**  
   Used filters and conditional formatting to detect blank, invalid, or inconsistent values.

3. **Data Correction**  
   Addressed invalid (`ERROR`, `UNKNOWN`) and missing (blank) entries by cross-referencing related columns to infer correct values. For example:  
   - If **Item** was known but **Price Per Unit** was missing, the price was corrected based on item metadata (e.g., *Cake* → **$3.00**)
   - If **Quantity** and **Price Per Unit** were valid but **Total Spent** was missing, it was recalculated as `Quantity × Price Per Unit`

4. **Data Deletion**  
   Removed rows that contained too many missing or invalid values, especially when the data could not be reliably inferred from other columns. This ensured the dataset remained accurate and trustworthy for analysis.

5. **Data Entry Restrictions**  
   Used Excel's Data Validation feature to restrict acceptable input values and prevent future errors.

6. **Data Type Correction**  
   Ensured all columns had the correct data type and consistent formatting:
   - Converted text-based numbers into numeric values using the VALUE function.
   - Formatted pricing fields to two decimal places (e.g., $3.00) for clarity and consistency.
   - Verified that date fields were properly recognized as Date values, enabling accurate filtering and time-based analysis.

7. **Outlier & Invalid Entry Checks**  
   Reviewed the dataset for outliers or illogical values — for example, items with incorrect pricing or unusually high totals. Such records were inspected and corrected based on reference data or consistent price patterns.

8. **Feature Engineering**  
   Derived new variables from existing columns to enhance the dataset for analysis:
   - Used VLOOKUP to categorize each item as either Food or Beverage based on a reference list.
   - Applied the TEXT function on Transaction Date to extract Transaction Day and Transaction Month, enabling time-based analysis and trend insights.

9. **Final Checks**  
   Performed a final review to ensure data completeness and accuracy:
   - Rechecked for any remaining invalid entries and blank cells.
   - Verified that all calculations, such as Total Spent, were accurate.
   - Applied a multi-level sort by Item and then by Transaction Date to organize the dataset logically, ensuring consistency and easier trend analysis.

---

## 📈 Key Results
- Reduced invalid or inconsistent entries
- Created clean, analysis-ready data with standardized formats
- Produced pivot summaries to highlight monthly sales trends and top-performing items

---

## 🎓 Skills Demonstrated
- **Data Quality Assessment** – Identified inconsistencies, missing values, and invalid entries across 10,000 rows
- **Data Cleaning & Transformation** – Applied Excel functions (`TRIM`, `CLEAN`, `VALUE`, `TEXT`, `VLOOKUP`) to standardize and correct data
- **Data Validation** – Implemented validation rules and conditional formatting to ensure data integrity
- **Feature Engineering** – Created derived variables (Category, Transaction Day, Transaction Month) to enable deeper analysis
- **Logical Problem-Solving** – Cross-referenced columns to infer and correct missing or invalid data using business logic
- **Documentation** – Maintained detailed cleaning logs and data dictionaries for reproducibility and transparency
- **Data Analysis** – Built pivot tables to summarize sales trends and identify top-performing items

---

## 📂 Repository Structure
| Folder/File | Description |
|--------------|-------------|
| `data/raw_data.xlsx` | Original uncleaned dataset |
| `data/cleaned_data.xlsx` | Final cleaned dataset with pivot table summaries |
| `documentation/data_cleaning_log.xlsx` | Step-by-step record of cleaning actions |
| `documentation/data_dictionary.xlsx` | Explains data columns, formats, and meanings |

---

## 🧭 How to View
- You can view Excel files directly in GitHub's preview or download them for full access.  
- Open the `.xlsx` files in Microsoft Excel to explore formulas, validation, and pivot tables.

---

## 👤 Author
**Muhammad Fikri Bin Mohd Roslee**  
📫 https://www.linkedin.com/in/fikriroslee/  
💼 https://github.com/fikriroslee

---

## 🏷️ Keywords
`Excel` · `Data Preparation` · `Data Cleaning` · `Data Validation` · `Feature Engineering` · `Pivot Tables`
