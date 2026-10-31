# Customer Churn Analysis

**Author: Thato Mafego**

## Project Overview

In this project, I explored customer churn in a telecommunications dataset. I used Python to prepare the customer records, calculate churn and retention metrics, and compare churn rates across customer groups. The aim was to identify patterns that could help a business improve customer retention.

This is an exploratory analysis. It summarizes patterns in the available data; it does not train a machine learning model or predict which individual customers will leave.

## Objectives

- Measure the overall churn and retention rates.
- Compare churn across customer tenure and contract types.
- Explore how internet service, support options, payment methods, and monthly charges relate to churn.
- Visualize the results and identify customer groups that may need further investigation.
- Recommend practical retention actions based on the analysis.

## Tools and Technologies

- **Power BI Desktop** for the interactive dashboard and KPI reporting
- **Python** for data preparation and exploratory analysis
- **pandas** and **NumPy** for cleaning and numerical analysis
- **Matplotlib** and **Seaborn** for notebook visualizations
- **Jupyter Notebook** for documenting the analysis
- **CSV** for the source and cleaned datasets

## Dataset

The project uses the Telco Customer Churn dataset. Each row represents a customer and includes service subscriptions, account and contract information, tenure, monthly and total charges, and churn status.

- Source file: `dataset/WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Cleaned output: `dataset/Telco_Customer_Churn_cleaned.csv`
- Customers analyzed: 7,043
- Columns in the cleaned output: 24, including three analysis fields created in the notebook

## Data Preparation and Analysis

I reviewed the dataset structure, data types, missing values, and duplicate records. I converted `TotalCharges` to a numeric field and filled blank values with zero for customers with no recorded tenure. I also created a numeric churn flag and grouped customers into tenure and monthly charge bands.

I compared churn rates across tenure groups, contract types, payment methods, internet services, support and security features, senior-citizen status, and monthly charge bands. I used grouped summaries, bar charts, box plots, and a tenure-by-charge comparison to examine these patterns. The cleaned dataset is saved as a CSV from the notebook.

## Key Performance Indicators

| KPI | Result |
|---|---:|
| Customers | 7,043 |
| Customers churned | 1,869 |
| Overall churn rate | 26.54% |
| Retained customers | 5,174 |
| Retention rate | 73.46% |
| Average monthly charges for churned customers | $74.44 |
| Average monthly charges for retained customers | $61.27 |

## Dashboard Features and Analysis

I built the customer churn dashboard in Power BI Desktop and saved the report as `dashboard/Task2_dashboard.pbix`. It presents the overall churn picture and allows the results to be explored across customer and service segments. The report includes headline customer and churn KPIs, churn comparisons by contract and tenure, and breakdowns by service, support, and payment characteristics. I also included a dashboard preview image at `dashboard/Task2_dashboard.png`.

The report is based on the cleaned Telco dataset. Its charts are descriptive and help compare groups; they do not establish that a particular service or customer characteristic causes churn.

## Key Findings

- Customers in their first 12 months had the highest tenure-group churn rate at **47.44%**. The rate declined across longer-tenure groups, reaching **6.61%** for customers with 61–72 months of tenure.
- Month-to-month customers had a **42.71%** churn rate, compared with **11.27%** for one-year contracts and **2.83%** for two-year contracts.
- Customers paying by electronic check had a **45.29%** churn rate, higher than the rates for the other payment methods in the dataset.
- Churn was **41.89%** among customers with fiber-optic internet service and **18.96%** among DSL customers. Customers with no internet service had a lower rate of **7.40%**.
- Customers without Tech Support had a **41.64%** churn rate, compared with **15.17%** among customers with Tech Support.
- Churned customers had higher average monthly charges (**$74.44**) than retained customers (**$61.27**), and a shorter median tenure (**10 months** compared with **38 months**).

These are observed associations in this dataset. They do not show that any single service, payment type, or charge level causes churn.

## Business Recommendations

- Focus retention outreach on newer customers, especially during their first year.
- Review the month-to-month customer experience and consider whether clear longer-term plan benefits could improve retention.
- Investigate the reasons for elevated churn among electronic-check and fiber-optic customers, including billing experience, pricing, and service quality.
- Promote support and security options where they meet customer needs, and evaluate whether access or onboarding barriers affect adoption.
- Review customer bills and service bundles for customers with high monthly charges.
- Track churn and retention metrics over time to assess whether retention actions are associated with improvement.

## Project Structure

```text
FUTURE_DS_02/
├── dataset/
│   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   └── Telco_Customer_Churn_cleaned.csv
├── notebook/
│   └── Task_2.ipynb
├── dashboard/
│   ├── Task2_dashboard.pbix
│   └── Task2_dashboard.png
└── README.md
```

To open the interactive report, download `dashboard/Task2_dashboard.pbix` and open it in Power BI Desktop. If prompted, point the data source to `dataset/Telco_Customer_Churn_cleaned.csv`.

## Skills Demonstrated

- Data quality checks and cleaning
- Handling missing and non-numeric values
- Exploratory data analysis
- Churn and retention KPI calculation
- Customer segmentation and grouped comparisons
- Data visualization with Matplotlib and Seaborn
- Turning analysis results into practical business recommendations
