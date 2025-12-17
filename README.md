# Syrian Telecom Customer Churn Analytics

## 📌 Project Overview
In the competitive telecommunications industry, customer churn—the phenomenon where customers stop using a service—directly impacts market share and revenue. This project utilizes a data-driven approach to analyze SyriaTel customer data, shifting from a reactive to a proactive retention strategy. By identifying predictable patterns in customer behavior, we aim to intervene before a customer decides to leave.

## 🎯 Business Objectives
* **Identify Patterns:** Discover specific customer characteristics and usage behaviors that signal an impending decision to churn.
* **Predictive Modeling:** Build and evaluate machine learning classifiers to accurately predict "at-risk" customers.
* **Actionable Insights:** Provide the marketing and retention teams with a prioritized list of customers likely to churn to facilitate targeted interventions.

## 📊 Data Summary
The analysis was conducted on a dataset containing **3,333 customer records** with **21 features**.
* **Key Findings from EDA:**
    * No missing or duplicate values were found in the dataset.
    * Feature set includes usage metrics (minutes, calls, charges) and account details (international and voice mail plans).
* **Data Preparation:** * Dropped redundant identifiers: `state`, `area code`, `phone number`, and `number vmail messages`.
    * Applied **One-Hot Encoding** to categorical variables (`international plan`, `voice mail plan`).
    * Scaled numerical features for optimal model performance.

## 🤖 Modeling & Evaluation
Two primary models were developed to predict churn:

| Metric | Decision Tree (Baseline) | Logistic Regression (Tuned) |
| :--- | :--- | :--- |
| **Accuracy** | **0.92** | 0.86 |
| **Recall (Churn)** | **0.75** | **0.82** |
| **Precision (Churn)**| **0.73** | 0.56 |

### **Key Takeaway:** The **Decision Tree** was selected as the final model because it provided a superior balance of results. While the tuned Logistic Regression had a higher recall (+0.60 increase), it suffered a significant drop in precision and overall accuracy. The Decision Tree's ability to maintain high accuracy (0.92) while reliably locating churning customers makes it the better choice for deployment.

## 💡 Key Business Insights
Based on the data analysis, the following patterns were identified as major churn drivers:
1. **International Plans:** Most customers who churn have an international plan; these customers require better, more competitive offers.
2. **Usage Rates:** High usage in both day and night categories correlates with churn; these segments should be offered better rates.
3. **Customer Service Interaction:** Frequent calls to customer care is a strong predictor of churn, indicating a need for improved service resolution.

## 🚀 Recommendations
* **Targeted Retention:** Implement loyalty incentives specifically for customers with high day/night usage and those on international plans.
* **Service Quality:** Monitor customers who call support more than three times and trigger a proactive outreach to resolve their issues.
* **Proactive Strategy:** Deploy the Decision Tree model to generate weekly "At-Risk" lists for the marketing team to offer personalized discounts.

---
*Developed as part of the SyriaTel Customer Retention Initiative.*