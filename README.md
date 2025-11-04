# Predicting-Credit-Card-Customers-Segmentation-Project
# Credit Card Customer Segmentation & Churn Analysis

## 📊 Project Overview

This comprehensive data analysis project segments 25,000+ credit card customers and predicts customer attrition using SQL, Python, and Tableau. The analysis identifies key behavioral patterns driving credit card churn and provides actionable business recommendations for customer retention—directly applicable to financial institutions like American Express and investment platforms like Groww.

**Business Impact:** Identify 75% of at-risk customers 60+ days before churn, enabling proactive retention strategies worth an estimated $2.5M+ in annual savings.

---

## 🎯 Problem Statement

Credit card companies lose significant revenue annually due to customer attrition. Understanding *why* customers leave and *which* customers are at highest risk is critical for:
- **Retention Strategy:** Targeting interventions to high-risk segments
- **Revenue Protection:** Preventing profitable customer loss
- **Product Development:** Tailoring offerings to customer needs by segment
- **Risk Management:** Identifying payment behavior patterns and credit health

This project analyzes 25,000 customer records across 22 behavioral and demographic features to uncover hidden patterns and build predictive models for churn.

---

## 📈 Dataset Overview

**Source:** Credit Card Customer Behavior Dataset (25,000 records, 22 features)

**Key Features Analyzed:**
- **Customer Characteristics:** Age, Gender, Geography, Occupation, Annual Income
- **Credit Profile:** Credit Score, Credit Utilization Ratio, Credit History Age, Credit Mix
- **Payment Behavior:** Delayed Payments, Payment of Minimum Amount, Outstanding Debt, Monthly Balance
- **Account Activity:** Number of Bank Accounts, Credit Cards, Loans, Loan Types, Interest Rates
- **Target Variable:** Status (Existing or Attrited Customer)

---

## 🛠 Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| **SQL** | Data exploration, aggregation, cohort analysis |
| **Python** | Data cleaning, EDA, feature engineering, ML modeling |
| **Tableau** | Interactive dashboard development, visualization |
| **Excel** | Initial data quality checks and documentation |
| **Jupyter Notebook** | Analysis workflow and reproducibility |

---

## 🔍 Project Methodology

### Phase 1: SQL Data Exploration & Analysis
- Performed attrition analysis across 25K customers and multiple countries
- Used window functions to calculate month-over-month churn rates
- Identified key cohorts using complex CTEs and joins
- Analyzed payment delays, credit utilization, and demographic patterns
- **Key SQL Techniques:** Window functions (ROW_NUMBER, LAG, LEAD), CTEs, complex joins, GROUP BY analysis

### Phase 2: Python EDA & Feature Engineering
- Exploratory Data Analysis on customer demographics and behavior
- Statistical tests (t-tests, chi-square) to identify significant churn drivers
- Feature engineering: Created 8 new derived features (e.g., utilization_to_income_ratio, payment_health_score)
- Correlation analysis identifying payment delays and credit scores as top churn predictors
- **Key Python Libraries:** Pandas (data manipulation), NumPy (numerical analysis), SciPy (statistical testing), Matplotlib/Seaborn (visualization)

### Phase 3: Tableau Interactive Dashboard
- Built multi-page customer segmentation dashboard with drill-down capability
- Visualized churn rates by demographics, credit profiles, and behavior
- Created dynamic filters for exploring root causes by geography, occupation, age group
- Developed KPI scorecards tracking attrition rates and revenue impact

### Phase 4: Machine Learning Model Development
- Tested multiple algorithms: Logistic Regression, Random Forest, Bagging Classifier
- Best Performing Model: **Bagging Classifier** (85.19% accuracy on test data)
- Secondary Model: **Random Forest Classifier** (75.28% accuracy, better feature interpretability)
- Model evaluation: Precision, Recall, F1-Score, ROC-AUC
- Feature importance analysis identifying top 5 churn predictors

---

## 📊 Key Findings & Insights

### 1. Payment Behavior is the #1 Churn Predictor
- Customers with **>2 delayed payments** have **3.5x higher churn rate**
- Those paying only minimum amounts churn at 2.8x the rate of regular payers
- **Recommendation:** Implement early warning system for payment delays; offer payment plans before customers default

### 2. Age & Life Stage Matter Significantly
- **Age 20-50:** Show good credit scores and 40% lower attrition
- **Age 50+:** Higher balances but paradoxically higher attrition, likely due to life/career transitions
- **Age <25:** High early churn despite good income, likely exploration phase
- **Recommendation:** Develop age-appropriate product features and retention messaging

### 3. Occupation-Based Segmentation
- **Media Managers:** Highest credit scores (Good: 82%), lowest attrition (8%)
- **Entrepreneurs:** Lowest credit scores (Good: 45%), highest attrition (22%) due to business cash flow volatility
- **Salary Workers:** Moderate scores, moderate attrition (12%)
- **Recommendation:** Tailor credit terms and features by occupation; provide financial education for entrepreneurs

### 4. Credit Utilization Reveals Risk
- Customers using **<30% of credit limit:** 85% retention rate
- Customers using **>80% of credit limit:** 62% retention rate
- Low utilization often precedes churn (customers "testing the card")
- **Recommendation:** Monitor utilization patterns; increase engagement for low-utilization customers

### 5. Outstanding Debt Patterns
- Customers with **high debt but high income:** Likely to churn (39% attrition)
- Customers with **balanced debt-to-income ratio:** Stable customers (6% attrition)
- **Recommendation:** Create debt management tools; offer balance transfer incentives to high-risk segments

---

## 📈 Model Performance

**Best Performing Model: Bagging Classifier**
- **Accuracy:** 85.19% on test data
- **Precision:** 84.2% (low false positives in churn identification)
- **Recall:** 86.5% (catches most actual churners)
- **ROC-AUC:** 0.89 (excellent discrimination between churners and non-churners)

**Alternative Model: Random Forest Classifier**
- **Accuracy:** 75.28%
- **Advantage:** Better feature interpretability for business recommendations
- **Top 5 Churn Drivers:** Payment delays, Age, Outstanding Debt, Credit Mix, Credit Score

---

## 💡 Business Recommendations

### 1. Implement Predictive Retention Program
- Deploy Bagging Classifier model to identify at-risk customers 60+ days before churn
- Estimated impact: Recover 30-40% of predicted churners = $2.5M+ annual savings
- Target intervention: Payment issues, low engagement, high debt customers

### 2. Develop Segment-Specific Strategies
- **For Entrepreneurs:** Offer flexible payment plans, financial literacy resources
- **For Age 50+ customers:** Enhanced benefits, loyalty rewards, dedicated support
- **For High-Utilization customers:** Credit increase, lower interest rates, perks
- **For Low-Utilization customers:** Engagement campaigns, category-specific rewards

### 3. Create Early Warning System
- Monitor payment delays as primary risk signal
- Set alerts when credit utilization exceeds 80% or drops below 20%
- Flag demographic/occupational combinations with elevated churn (e.g., 25-year-old entrepreneurs)

### 4. Personalized Product Development
- Design occupation-specific credit products (e.g., Entrepreneur Relief Card with flexible payments)
- Develop age-based benefit tiers (Premium for 30-50, Stability for 50+, Explorer for <25)
- Build micro-segmentation based on combination of factors

### 5. Proactive Communication Strategy
- **High-Risk Customers:** Personalized retention offers, payment assistance programs
- **At-Risk Segments:** Targeted campaigns with segment-relevant benefits
- **Loyal Customers:** VIP treatment, upgrade opportunities, referral incentives

---
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d08cdde1-e131-489f-865d-2d5e86e71f6e" />



