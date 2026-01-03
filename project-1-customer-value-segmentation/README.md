# Customer Value Analysis & Segmentation for ElectroMart

## Business Problem
ElectroMart, an online electronics retailer, invests heavily in promotions and customer retention but lacked clarity on what truly drives customer spending and long-term value.  
The objective of this project was to identify the behavioral factors that influence customer value, predict high vs low value customers, and develop actionable customer segments to support targeted marketing strategies.

## Data Overview
- Transaction-level customer purchase data
- Behavioral variables including product type, quantity, add-ons, shipping method, payment method, seasonality, and ratings
- Demographic variables were initially explored but excluded after statistical testing showed no significant impact on spending

## Methodology
1. **Data Preparation**
   - Cleaned and transformed date variables to create seasonal indicators
   - Classified customers as high- or low-value using median total spending to account for right-skewed distributions
   - Encoded categorical variables for analysis

2. **Exploratory Data Analysis (EDA)**
   - Analyzed spending distributions and key behavioral variables
   - Identified patterns across product categories, add-ons, and seasonal effects

3. **Hypothesis Testing**
   - Tested relationships between spending and product categories, add-ons, and seasonality
   - Found statistically significant differences in spending across product types and strong interaction effects between product category and season
   - Determined that behavioral variables, not demographics, drive customer value

4. **Predictive Modeling**
   - **Linear Regression:** Predicted total spending using behavioral features
   - **Logistic Regression:** Classified customers as high- or low-value (accuracy ≈ 82%)
   - **Decision Tree:** Captured non-linear patterns and improved classification accuracy (≈ 88%)

5. **Customer Segmentation**
   - Applied k-means clustering (k = 3) using behavioral features
   - Identified three actionable customer segments:
     - *Low-Spend Efficient Buyers*
     - *Add-On Lovers / Accessory-Heavy Buyers*
     - *Bulk & High-Value Buyers*
   - Strong alignment observed between predictive classifications and clusters

## Key Insights
- Customer value is driven by **behavioral factors**, not demographics
- Product category and seasonality have a significant interaction effect on spending
- Add-on purchases and quantity strongly differentiate high-value customers
- Decision trees outperformed logistic regression in capturing non-linear spending behavior

## Business Recommendations
- Shift marketing segmentation from demographics to behavioral signals
- Target high-value and bulk buyers with premium offers and early product access
- Increase attachment rates for add-on–heavy customers using bundles and checkout prompts
- Use decision tree rules to automate personalized marketing flows
- Introduce behavior-based tiered benefits rather than demographic-based loyalty programs

## Tools Used
Python (pandas, numpy, matplotlib, seaborn, scikit-learn, statsmodels)

