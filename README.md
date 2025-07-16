# Telco Customer Churn Analysis

## Project Overview
This project analyzes a Telco Customer Churn dataset to identify key drivers behind customer attrition. Using data processing, machine learning, and visualization, the goal is to help telecom companies improve retention strategies.

**Tools & Technologies Used:**
Python, Google Sheets, Google Looker Studio, Github Pages
<div align="center">
  <img src="https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/screenshot/Tech%20Stack.jpg">
</div>

## Project Structure

The repository is organized as follows:
* `Telco_Churn_Analysis.ipynb`: Core Python notebook.
* `WA_Fn-UseC_-Telco-Customer-Churn.csv`: Original dataset (from Kaggle).
* `telco_churn_processed_for_looker.csv`:  Cleaned dataset for dashboard.
* `screenshots/`:  Key visuals and outputs.
* `index.html`: TMain project page hosted on GitHub Pages.

## Methodology and Key Steps

1.  **Data Acquisition:**
    * Sourced dataset from Kaggle and reviewed data types.

2.  **Data Processing & Feature Engineering (using Python in Google Colab):**
    * Handled missing values, Standardized fields and unified ‘No service’ entries, Feature Creation:(Tenure_Group, MonthlyCharges_Category).
    * **Python Notebook:** [Link to Telco_Churn_Analysis.ipynb](https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/Telco_Churn_Analysis.ipynb)

3.  **Exploratory Data Analysis (EDA):**
    * Visualized churn trends across features like Contract Type, Tenure, Internet Service, Monthly Charges, and Payment Method using bar charts and box plots.
    ![Churn by Contract Type](https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/screenshot/Churn%20by%20Contract%20Type.jpg)
      
4.  **Machine Learning Model (Logistic Regression):**
    * Encoded categorical variables and split data (80% train, 20% test).
    * Trained Logistic Regression model to predict churn.
    * Evaluated using accuracy, precision, recall, and confusion matrix.
    * Analyzed feature coefficients to interpret churn drivers.

5.  **Interactive Dashboard (Looker Studio):**
    * Processed data uploaded to Google Sheets and connected to Looker Studio to build a dynamic dashboard.
    **Interactive Dashboard Link:** [View Live Dashboard](https://lookerstudio.google.com/u/0/reporting/0b5cb7b1-dc0c-475a-b5ab-9f63e0048543/page/irqOF)


## Key Findings & Business Insights

Based on the analysis, the following key insights were identified:

* **Contract Type:** Month-to-month customers churn more—long-term plans improve retention.
* **Tenure:** New customers (0-6 months) are most likely to churn—focus retention efforts early.
* **Internet Service:** Fiber optic users churn more—potential service issues.
* **Monthly Charges:** Higher charges correlate with higher churn—pricing strategy review suggested.
* **Payment Method:** Electronic check users churn at higher rates.


## Author

[Kratika Garg]
[LinkedIn Profile Link](https://www.linkedin.com/in/kratikagarg01/)]
[Medium / Blog Link](https://medium.com/@kratikagarg99/from-raw-data-to-business-insight-my-first-data-analytics-project-on-telco-churn-a-beginners-30270b9c7e5f)

