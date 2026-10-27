# Indonesian Online Lending Data Analysis

## About the Project
This project focuses on data preprocessing and exploratory data analysis (EDA) of an Indonesian online lending dataset. The analysis explores borrower characteristics, loan purposes, lending platform classifications, interest rates, and loan repayment statuses.

**This project was developed as part of the Mid-Term Examination for the Data Science Research Method course.**
The project applies Python-based data analysis techniques to identify patterns, examine data quality, and investigate potential relationships between lending platform status and borrower repayment behavior.

## Objectives
The main objectives of this project are:
- Perform data preprocessing to identify and handle missing values.
- Detect potential outliers using boxplots and the Interquartile Range (IQR) method.
- Apply Label Encoding to categorical variables.
- Standardize selected numerical variables.
- Visualize borrower characteristics and loan purpose distributions.
- Compare the distribution of records across legal, illegal, and unverified lending platform categories.
- Analyze average daily interest rates across lending platforms.
- Examine the distribution of loan statuses across platform categories.
- Investigate inconsistencies between loan tenor, disbursal dates, and due dates.

## Dataset Description
The dataset contains transaction-level information related to Indonesian online lending activities.
The variables include:
- `Transaction_ID`
- `Platform_Name`
- `Borrower_Age`
- `Borrower_Income`
- `Loan_Purpose`
- `Principal_IDR`
- `Tenor_Days`
- `Daily_Interest_Rate_Pct`
- `Admin_Fee_IDR`
- `Late_Penalty_IDR`
- `Total_Repayment_IDR`
- `Disbursal_Date`
- `Due_Date`
- `Loan_Status`
The dataset was provided for academic analysis. Platform classifications and findings should be interpreted in accordance with the reference sources and limitations of the dataset.

## Tools and Libraries
This project uses the following tools and Python libraries:
- Python
- Pandas — data manipulation and analysis
- NumPy — numerical operations
- Matplotlib — data visualization
- Seaborn — statistical visualization
- Scikit-learn — Label Encoding and numerical standardization

## Methodology
### 1. Data Preprocessing
Missing values were examined and handled using appropriate imputation methods. Median imputation was applied to selected numerical variables, while mode imputation was used for selected categorical variables.
The relationship between `Tenor_Days`, `Disbursal_Date`, and `Due_Date` was examined separately because these variables are mathematically related.
### 2. Outlier Detection
Boxplots and the IQR method were used to identify potential outliers in numerical variables, including loan principal, administrative fees, late penalties, and total repayment amounts.
### 3. Label Encoding
Categorical variables were converted into numerical representations using Scikit-learn's `LabelEncoder`.
### 4. Data Standardization
Selected numerical variables were standardized using `StandardScaler`. Separate DataFrames were maintained to preserve the cleaned data and encoded data.
### 5. Exploratory Data Analysis
EDA was performed using tables, pie charts, and bar charts to investigate:
- Distribution of borrower age groups.
- Distribution of borrower occupation categories.
- Distribution of loan purposes.
- Distribution of legal, illegal, and unverified platform categories.
- Average daily interest rates by lending platform.
- Loan status distribution by platform status.
- Consistency between recorded loan tenor and date differences.

## Key Areas of Investigation
### Lending Platform Classification
Platforms were categorized as Legal, Illegal, or Unverified using the reference classifications applied in the analysis. These classifications should be verified against official OJK and Satgas PASTI sources before being interpreted as definitive legal status.
### Loan Repayment Behavior
Loan statuses were compared across platform categories to explore whether the observed proportion of late payments differed between legal and illegal platforms.
The analysis is descriptive and does not establish a causal relationship between platform classification and repayment outcomes.
### Date and Tenor Consistency
The recorded loan tenor was compared with the number of days between disbursal and due dates. This investigation identified inconsistencies that may affect the reliability of further analysis.

## Repository Structure

```text
indonesian-online-lending-analysis/
│
├── midexam_indonesian_pinjol_analyst_dataset.csv
├── Pinjol_Analysis.ipynb
└── README.md
```
## Limitations
- The analysis depends on the quality and completeness of the provided dataset.
- Some records contain inconsistencies between loan tenor and date variables.
- Platform classifications depend on the reference sources used and their applicable dates.
- Observed associations do not establish causation.
- Results may not be generalizable to all Indonesian online lending platforms or borrowers.

## Academic Context
**Course:** Data Science Research Method  
**Assessment:** Mid-Term Examination  
**Project:** Data Preprocessing and Exploratory Data Analysis of an Indonesian Online Lending Dataset

This repository documents the Python code, preprocessing procedures, and visualizations developed for the examination.

## Disclaimer
This project is intended for academic and educational purposes only. The findings represent patterns observed in the provided dataset and should not be interpreted as definitive conclusions about all online lending platforms in Indonesia.

## Author

Created as part of the Mid-Term Examination for Data Science Research Method.
