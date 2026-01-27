# Customer Value Analysis & Segmentation for ElectroMart

## **Business Problem:**

ElectroMart, an online electronics retailer, invests significantly in promotions and customer retention initiatives but lacked clear insight into which customer behaviors truly drive spending and long-term value. Existing strategies relied on broad targeting, resulting in inefficient resource allocation and limited personalization.

## **Project Objective**
To identify the behavioral drivers of customer value, accurately predict high- vs. low-value customers, and develop actionable customer segments to support data-driven marketing, retention, and loyalty strategies.

## **Research Questions:**

1. Which behavioral and transactional variables (e.g., product type, quantity, add-ons, payment method, etc) most strongly influence customer spending and value?

2. How effectively can supervised machine learning models classify customers into high-value and low-value groups using behavioral data?

3. What meaningful customer segments emerge from unsupervised learning, and how do these segments differ?

4. How can insights from predictive modeling and clustering inform targeted marketing strategies, loyalty program design, and customer experience improvements?

## **Data Overview:**
Behavioral variables including:
1. Product type
2. Quantity purchased
3. Add-on spending
4. Shipping method
5. Payment method
6. Seasonality
7. Customer ratings

Demographic variables like Age and Gender were initially explored but excluded after statistical testing showed no meaningful relationship with customer value or spending.

## **Methodology:**

**Data Preparation**
1. Cleaned and transformed transaction dates to create seasonal indicators.
2. Classified customers as high-value or low-value using median total spending to account for right-skewed revenue distributions.
3. Created binary codes for relevant columns like Gender.
4. Encoded categorical variables and standardized numeric features for modeling and clustering

**Exploratory Data Analysis (EDA)**
1. Analyzed spending distributions and customer purchasing patterns
2. Examined differences across product categories, add-on behavior, and ratings

**A. Hypothesis Testing**

Tested relationships between customer spending and: Product category / Add-on purchases / Seasonality

**B. Predictive Modeling**

**1. Linear Regression:** Modeled total spending using behavioral features

**2. Logistic Regression:** Classified customers into high- vs. low-value groups (Accuracy ≈ 82%)

**3. Decision Tree Classifier:** Captured non-linear behavior patterns (Accuracy ≈ 88%)
Decision trees provided the most interpretable and actionable rules for identifying value-driving behaviors

**C. Customer Segmentation**

Applied k-means clustering (k = 4) using behavioral features
Identified four distinct customer segments:

- Loyal Core Smartphone Buyers

- Add-On Revenue Drivers

- Low-Engagement Buyers

- High-Volume Transactional Buyers

Strong alignment observed between behavioral clusters and HighValue predictions, confirming that unsupervised segmentation naturally reflects customer value tiers

## **Key Insights:**
1. Customer value is driven by behavioral factors, not demographics
2. Purchase quantity, add-on spending, and product type are the strongest predictors of value
3. Product performance varies significantly by season, reinforcing the importance of timing in promotions and inventory planning.
4. High revenue does not always imply high satisfaction or loyalty
5. Decision trees outperform linear models in capturing complex customer behavior patterns

## **Business Recommendations:**
1. Shift marketing segmentation from demographic targeting to behavior-based strategies
2. Prioritize high-value and high-volume customers with premium service, early product access, and retention initiatives
3. Optimize add-on attachment rates through targeted bundles and checkout prompts for add-on–heavy customers
4. Use decision tree rules to automate personalized marketing and service interventions
5. Redesign loyalty programs to reward value-driving behaviors rather than static membership tiers
6. Align promotions and inventory decisions with seasonal product demand patterns

## **Tools Used**

**Data Analysis & Manipulation**

- pandas, numpy

- Statistics & Econometrics: scipy.stats, statsmodels (api, formula.api), variance_inflation_factor

**Visualization**

- matplotlib

- seaborn

- plotnine (ggplot-style)

**Machine Learning (scikit-learn)**

- **Preprocessing:** ColumnTransformer, OneHotEncoder, StandardScaler

- **Model training:** train_test_split

- **Regression:** LinearRegression, Lasso

- **Classification:** LogisticRegression, DecisionTreeClassifier

- **Model validation:** cross_val_score, KFold

- **Evaluation:** mean_squared_error, accuracy_score, confusion_matrix

- **Clustering:** KMeans

- **Decision tree visualization:** plot_tree

