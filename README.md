# Telco Customer Churn Analysis

## Project Overview

This project focuses on analyzing a comprehensive Telco Customer Churn dataset to identify key factors contributing to customer attrition. The primary goal is to leverage data processing, machine learning, and interactive visualization techniques to extract actionable insights that can help telecommunication companies reduce customer churn and improve retention strategies.

**Tools & Technologies Used:**
* **Python:** Data cleaning, feature engineering, exploratory data analysis (EDA), and machine learning (Logistic Regression).
* **Google Colaboratory:** Cloud-based Jupyter environment for Python development.
* **Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn:** Core Python libraries for data manipulation, visualization, and modeling.
* **Google Sheets:** Intermediate data storage for connecting to Looker Studio.
* **Google Looker Studio (formerly Data Studio):** For building interactive dashboards and visualizations.
* **GitHub Pages:** For hosting the project portfolio and documentation.
<div align="center">
  <img src="https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/screenshot/Tech%20Stack.jpg">
</div>

## Project Structure

The repository is organized as follows:
* `Telco_Churn_Analysis.ipynb`: The Google Colab notebook containing all Python code for data processing, EDA, and model building.
* `WA_Fn-UseC_-Telco-Customer-Churn.csv`: The original raw dataset downloaded from Kaggle.
* `telco_churn_processed_for_looker.csv`: The cleaned and feature-engineered dataset used for the Looker Studio dashboard.
* `screenshots/`: A directory containing various screenshots of the Looker Studio dashboard and key Python outputs.
* `index.html`: The main portfolio page hosted on GitHub Pages, linking to the dashboard and this repository.

## Methodology and Key Steps

1.  **Data Acquisition:**
    * Obtained the Telco Customer Churn dataset from Kaggle.
    * Initially reviewed the dataset structure and data types.

2.  **Data Processing & Feature Engineering (using Python in Google Colab):**
    * **Handling Missing Values:** Converted 'TotalCharges' to numeric, replacing non-numeric (blanks) with 0, assuming these are new customers.
    * **Standardization:** Transformed `SeniorCitizen` (0/1) to 'No'/'Yes' for better readability. Standardized 'No internet service' and 'No phone service' entries across related columns to 'No'.
    * **Feature Creation:**
        * `Tenure_Group`: Categorized customer tenure into distinct groups (e.g., '0-6 Months', '7-12 Months').
        * `MonthlyCharges_Category`: Segmented monthly charges into 'Low', 'Medium', 'High', 'Very High'.
        * `Has_MultipleServices`: A binary indicator if a customer subscribes to both phone and internet (excluding no internet service).
    * **Data Retention:** Ensured `customerID` was retained in the final processed CSV for accurate counting and distinct customer identification in Looker Studio.
    * **Python Notebook:** [Link to Telco_Churn_Analysis.ipynb](https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/Telco_Churn_Analysis.ipynb)

3.  **Exploratory Data Analysis (EDA) & Visualization (using Python):**
    * Conducted visual analysis to understand relationships between features and churn.
    * Generated various plots (e.g., bar charts, box plots) to highlight churn patterns across `Contract Type`, `Tenure_Group`, `InternetService`, `MonthlyCharges`, and `PaymentMethod`.
    * **Example EDA Plot:**
    * 
        ![Churn by Contract Type](https://github.com/kratikaatgithub/telco-customer-churn-analysis/blob/main/screenshot/Churn%20by%20Contract%20Type.jpg)
      
4.  **Basic Machine Learning Model (Logistic Regression):**
    * Converted the `Churn` target variable to numerical (No=0, Yes=1).
    * Applied one-hot encoding to handle categorical features, preparing data for the model.
    * Split data into training and testing sets (80% train, 20% test).
    * Trained a Logistic Regression model to predict customer churn likelihood.
    * Evaluated model performance using accuracy, classification report (precision, recall, f1-score), and confusion matrix.
    * Analyzed model coefficients to identify features with the strongest impact on churn prediction.

5.  **Interactive Dashboard (using Google Looker Studio):**
    * Uploaded the processed data (`telco_churn_processed_for_looker.csv`) to Google Sheets.
    * Connected Looker Studio to the Google Sheet as the data source.
    * Designed an interactive dashboard with key performance indicators (KPIs) and charts.
    * Included scorecard for overall churn rate, bar charts for churn by demographics and service types, and filter controls for dynamic analysis.
    * **Interactive Dashboard Link:** [View Live Dashboard](https://lookerstudio.google.com/u/0/reporting/0b5cb7b1-dc0c-475a-b5ab-9f63e0048543/page/irqOF)


## Key Findings & Business Insights

Based on the analysis, the following key insights were identified:

* **Contract Type:** Customers on `Month-to-month` contracts show a significantly higher churn rate compared to those on `One year` or `Two year` contracts. This highlights the importance of encouraging longer-term commitments.
* **Tenure:** New customers, especially those in the `0-6 Months` tenure group, have the highest propensity to churn. Retention efforts should be front-loaded.
* **Internet Service:** Customers with `Fiber optic` internet service churn at a much higher rate than those with `DSL` or no internet service. This suggests potential issues with fiber optic service quality or perceived value.
* **Monthly Charges:** Churned customers tend to have higher average `MonthlyCharges`, indicating that price perception or value for money could be a factor.
* **Payment Method:** `Electronic check` is associated with a particularly high churn rate, suggesting friction or dissatisfaction with this payment method.
* **Senior Citizens:** (Add insight about SeniorCitizen based on your EDA, if any, or remove if not significant).
* **Model Insights (from Logistic Regression coefficients):** (Summarize 2-3 most influential features from your model's coefficients output in Cell 6. For example: "The model identified `Contract_Month-to-month` and `InternetService_Fiber optic` as strong positive predictors of churn, while `tenure` and `Contract_Two year` were strong negative predictors.")

## Future Enhancements

* Explore more advanced machine learning models (e.g., Random Forest, Gradient Boosting) for improved churn prediction accuracy.
* Perform deeper text analysis on customer feedback (if available) to understand qualitative reasons for churn.
* Implement A/B testing for new retention strategies suggested by the insights.
* Integrate real-time data sources for continuous monitoring of churn risk.

## Author

[Kratika Garg]
[LinkedIn Profile Link](https://www.linkedin.com/in/kratikagarg01/)]
[Optional: Medium / Blog Link]

