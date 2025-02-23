# SyriaTel-Customer-Churn-Predcition-Model
## 📖 Overview
The primary goal of this project is to develop a predictive model that identifies customers at risk of churning from SyriaTel, a telecommunications company. By analyzing customer behavior and usage patterns, the company can take proactive measures to retain customers, ultimately reducing revenue loss and increasing customer lifetime value.

---

## 📊 Problem Statement  
SyriaTel, a telecommunications company, is trying to maximize its customer retention while minimizing the retention costs which in turn maximizes profits.
The problem is that the company experiences customer churn, which negatively impacts revenue and business stability.  

**Key Question:** What are the primary factors influencing customer churn?

---

## 🎯 Objectives
The main objective of this project is to build a predictive model that can identify customers who are likely to stop doing business with SyriaTel.

**Secondary Objectives**
- To analyze customer usage patterns and behaviors that indicate a higher risk of churn.​
- To optimize the hyperparameters of our chosen model to improve performance and reduce false positives/negatives.​
- To evaluate how customer service interactions influence churn rates.

---

## Business and Data Understanding
### Stakeholder Audience
This analysis is aimed at business decision-makers, data analysts, and customer retention teams at SyriaTel. Understanding churn patterns allows these stakeholders to implement data-driven strategies to improve customer satisfaction and retention rates.

### Dataset Choice
The dataset used in this project was sourced from a publicly available Kaggle repository: [Churn in Telecoms Dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset). The dataset contains 3,333 customer records and 21 features, including:
- **Customer Information**: State, account length, area code, phone number.
- **Subscription Plans**: International plan, voicemail plan.
- **Usage Metrics**: Number of voicemail messages, total day/evening/night/intl minutes.
- **Call Records**: Total calls made during different times of the day, customer service calls.
- **Billing Details**: Charges incurred during different periods.
- **Churn Label**: A Boolean variable indicating if a customer churned (True) or not (False).

---

## Modeling
### Analytical Approach
The project followed a structured workflow:
1. **Data Understanding** - Assess dataset completeness and quality.
2. **Data Preparation** - Handle missing values, outliers, and class imbalances.
3. **Visualization** - Use bar plots and heat maps to explore patterns and correlations.
4. **Modeling** - Train multiple machine learning models and optimize the best-performing one.
5. **Insights** - Identify key factors influencing churn and derive actionable recommendations.

### Visualisations
#### Observation 1
Key Insights:​
- Texas (18), New York (16), and California (14) have the highest churn rates, suggesting possible dissatisfaction or competitive markets.​
- States with lower churn (e.g., South Dakota, Nebraska, and Kansas) may have more stable customer bases.​
- Targeted retention efforts should focus on high-churn states to understand and address the causes.​


#### Observation 2
Key Insight:
- Customers with an international plan churn at a higher rate than those without one.

#### Observation 3
Key Insights​:
- Having an international plan is the strongest indicator of churn, reinforcing earlier findings.​
- High customer service call frequency suggests dissatisfaction, making it a critical churn predictor.​
- Voice mail plan and customer engagement score also impact churn, indicating service usage patterns matter.​
- Geographic location meaning various states in the US plays a role, possibly due to regional service differences.

#### Observation 4
Key Insights​:
- Strong correlations exist between total minutes, total calls, and total charges for day, evening, and night categories but this is expected since charges are based on usage.​
- Customer service calls show little correlation with other features, meaning complaints might not be linked directly to call usage.

### Machine Learning Models Used
- **Logistic Regression**: F1 Score = 48.32%
- **Decision Tree**: F1 Score = 78.10%
- **Random Forest**: F1 Score = 82.42%
- **XGBoost**: F1 Score = 86.63% (Best-performing model)

Feature importance analysis revealed that total charge metrics, international plan subscription, and customer service call frequency were the strongest predictors of churn.

---

## Evaluation
- Despite achieving high accuracy with the XGBoost model, the project encountered challenges such as class imbalance (85.51% of customers did not churn vs. 14.49% who did). 
- I used hyperparameter tuning were used to mitigate this issue. 
- The evaluation of model performance was conducted using F1 scores to balance precision and recall.

---

## Conclusion
### Key Findings
1. Customers with **international plans** are more likely to churn.
2. High **total day and evening call charges** correlate with increased churn.
3. Frequent **customer service calls** indicate dissatisfaction and higher churn likelihood.
4. Churn rates vary by **geographical location**, with some states experiencing higher churn.

### Business Impact
- **Proactive customer retention strategies** can be implemented using the predictive model.
- **Targeted engagement efforts** can improve customer satisfaction and reduce churn.

---

## Recommendations
1. **Improve Customer Service** - Address issues proactively, enhance response quality, and reduce resolution time.
2. **Personalized Retention Offers** - Provide targeted discounts and customized plans for high-risk customers.
3. **International Plan Optimization** - Reevaluate pricing and benefits to reduce churn among international plan users.
4. **Customer Engagement Strategies** - Launch loyalty programs and personalized communication to enhance retention.
5. **Regional Strategy Implementation** - Investigate and address state-specific churn trends.

---

## 📂 **Repository Contents**  
- **Data**: The cleaned dataset and raw data files.  
- **Notebooks**: Jupyter Notebook used for data cleaning, exploration, visualization and modeling iterations.  
- **Visuals**: Graphs and charts generated during the analysis.
    [Tableu Link](https://public.tableau.com/views/SyriaTelCustomerChurnAnalysis/Sheet2?:language=en-GB&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
- **Presentation**: PowerPoint slides summarizing the project findings.
    [Presentation Link](https://1drv.ms/p/c/d9811d24aee7ad2a/ERvb2FtZTUNLlS-R40JGfncBwxZbXfWFaDaVTJ6C-xop8Q?e=cnBq9B)

## 🤝 **Acknowledgements**  
Thanks to all contributors and stakeholders for their input and support in making this project successful.  

---

## 📬 **Contact**  
For questions or feedback, feel free to reach out at langatchebetbev@gmail.com.