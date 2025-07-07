# Data Science Intern        |   Acorns | Irvine, CA | Fall 2017 

### What is Acorns? 

Acorns is a start-up financial technology company which aims to help millennials invest in the stock market by rounding up change from purchases made with debit cards. If you choose to sign up with Acorns, you connect your bank account to the platform and it uses the Plaid API (manages financial data on the transaction level) to understand how much money you spent. Say you spend $3.98 at Starbucks, the Acorns platform will round up your purchase spend to $4.00 and invest the $0.02 in mutual funds. This is a no hassle way for millennials to start investing. 

### What team or product did I work on? 

I was an intern on the data science team during the Fall. The data science team at the time consisted of PhD mathematicians who transitioned into data science proper and were learning how to use engineering software and tools to be effective with enterprise data.  

#### The Food Labeling Project 

I selected an intern project from a list of projects in the backlog of the data science team. I was interested in understanding the way that Acorns customers were spending money on food. As a company we had a large collection of transaction level data coming in from Plaid but the data was not labeled in a way that was meaningful enough to understand what food spending looked like.  

Understanding Merchants 

Merchants are the companies that customers are spending with. This could be Starbucks, or the local Café and it could also be Whole Foods or the Gas Station. Some companies are notable and international like McDonalds so it’s easy to identify the business category. Other companies are small or only available in Middle America so it’s more challenging to understand what the company sells. 

Understanding a Transaction 

Millennials use many different forms of payment but the only form of payment meaningful to the company Acorns is a checking account because of the ability for checking account holders to have cash available to use for a purchase in the account and the ability to pay for a purchase in the market with merchants. Savings or ATM accounts will only enable you to collect available cash from a machine and credit card hold lines or credit which are not cash, neither of these accounts are useful in this case.  

Transactions coming from a debit card have an amount, a date of purchase, and a merchant name. Here is a very generic example: 

3/12/2022 Starbucks - $3.96 

A typical bank statement will have many transactions but the way that the bank decided to format the transaction in the monthly statement might be different. A monthly statement could have many transactions from different merchants for varying amounts. 

3/1/2022 Starbucks - $3.96 

3/1/2022 Macy’s - $44.21 

3/2/2022 Starbucks - $3.96 

3/2/2022 McDonalds - $9.46 

If we examine the sample cluster of transactions above, what do you notice? This is the way the project started for me. I had a list of transactions for a sample period, and they were all food related purchases, but I wanted to understand more.  

I thought about a few high-level themes: 

- Frequency 
  - how often does this transaction appear each:
     - day
     - week
     - month
- Budget
  - in relation to other transactions on an individual statement what percentage of the total budget is this person spemding on this type of purchase?

- Tier
  - if this is a dinner transaction how would you classify the establishment
  - if this is a grocery store how would you classify the grocery store
  - if this is a coffe shop is it a large chain or a mom and pop shop
 
- Sub-category

  - Fast Food
  - Chain Restaurants
  - Coffee
  - Grocery
  - Meal Kits
  - Delivery

#### Unpacking Frequency 

#### Examining a Budget 

#### Thinking about Tier 

#### Creating A Sub-Category for a Transaction 

### The purpose of the project
I was invited to join this team after working on the team with Intuit where I explored transactional data on the categorizations teams. My new PI was trying to understand how the larger accounting form structured their databases and understand the types of machine learning models they were using to make spending recommendations. Unfortunately I am not sure I was very helpful for him given I was only working on the data engineering pipelines and I didnt look at the machine learning models explicitely. 

What I can say now given what I nave learned over time, is that it is really important to have a general question that you want to answer and then start making assumptions about how to answer that question with your data. 

### Exploratory data analysis

Exploratory Data Analysis (EDA) is the broad process in a data science project where you:
	•	Explore, summarize, and understand your data.
	•	Use univariate analysis to understand individual variables.
	•	Use bivariate and multivariate analysis to understand relationships between variables.

Where does EDA fit in a data science project?

	1.	Problem Definition – understanding the business question.
	2.	Data Collection & Cleaning – preparing data for analysis.
	3.	Exploratory Data Analysis (EDA) – univariate, bivariate, and multivariate analyses to uncover insights and prepare for modeling.
	4.	Modeling & Evaluation – building predictive or explanatory models.
	5.	Deployment & Monitoring – putting the model into production and tracking its performance.

 ### How my PI helped me understand EDA 
 Given the company was so new during this time, I was able to initiate the proejct and this was a real project with real stakeholders and real transactional data. I was familiar with looking at transactional data and understanding very generally the reasons why some transactions coming from financial institutions are improperly labeled but I did not understand much about the Food category specifically and the different types of customers or users.

I learned there are different types of users and they tend to spend money on food in a gew specific ways. Users who were more central to the US tend to spend their money on grocieries that are owned by one particular brand Kroger and that brand owned many different stores are across america. It became clear if a grocery purchase was coming from a set of states and the price was within a certain range this strore was a part of the kroger brand and the users income was predictable. Lower middle class incidividals tend to spend money at kroger while higher earning individuals tend to live places where there is a whole foods and have highers grocery budgets per month than lowre income earning individuals. when trying to make investment recommendations for these individuals there are going to be a bit different. 

### First phase of a data science project
The first phase of EDA focuses on understanding data structure, cleaning issues, distributions, and preliminary relationships to inform modeling decisions later.

1. Data Summarization

- Purpose: Quickly understand basic characteristics of each variable.
- Techniques:
	•	describe() in Python (mean, median, std, min, max, quartiles)
	•	Value counts for categorical variables

2. Missing Value Analysis

- Purpose: Identify and decide how to handle missing or null values.
- Techniques:
	•	Checking null counts
	•	Visualizing missing data patterns (e.g. using missingno library)

3. Univariate Analysis

- Purpose: Explore individual variables to understand their distributions.
- Techniques:
	•	Histograms for numerical data
	•	Bar plots for categorical data
	•	Box plots to identify outliers

4. Bivariate Analysis

- Purpose: Examine relationships between two variables.
- Techniques:
	•	Scatter plots (two numerical variables)
	•	Correlation matrix and heatmaps
	•	Grouped bar charts (categorical vs numerical)

5. Multivariate Analysis

- Purpose: Explore complex relationships among multiple variables.
- Techniques:
	•	Pair plots (seaborn pairplot)
	•	Grouped summaries (e.g. pivot tables)
	•	Crosstabs for multiple categorical variables

6. Outlier Detection

- Purpose: Identify data points that may skew analysis or models.
- Techniques:
	•	Box plots
	•	Z-score or IQR method

7. Data Visualization

- Purpose: Quickly reveal patterns, distributions, or anomalies.
- Techniques:
	•	Histograms, bar charts, scatter plots
	•	Heatmaps (for correlation)
	•	Violin plots or KDE plots for distribution shape

### second phase of a data sciencw project

The second phase focuses on modeling and evaluation, where data scientists build predictive models, optimize them, and assess their ability to perform well on unseen data to solve the business problem.

1. Feature Engineering

- Purpose: Create new variables or transform existing ones to improve model performance.
- Techniques:
	•	Encoding categorical variables (one-hot, label encoding)
	•	Scaling numerical features (standardization, normalization)
	•	Creating interaction terms or polynomial features
	•	Aggregating or binning features (e.g. age groups)

2. Model Selection

- Purpose: Choose appropriate algorithms based on problem type and data characteristics.
- Techniques:
	•	For classification: logistic regression, decision trees, random forests, XGBoost, SVM, neural networks
	•	For regression: linear regression, ridge/lasso regression, tree-based regressors

3. Model Training

- Purpose: Fit the selected models on training data.
- Techniques:
	•	Splitting data into training and validation sets
	•	Cross-validation (e.g. k-fold) to assess stability and generalizability

4. Model Evaluation

- Purpose: Assess how well models perform using appropriate metrics.
- Techniques:
	•	Classification metrics: accuracy, precision, recall, F1-score, ROC-AUC
	•	Regression metrics: RMSE, MAE, R²
	•	Confusion matrix analysis
	•	Residual analysis (for regression)

5. Hyperparameter Tuning

- Purpose: Optimize model performance by tuning parameters.
- Techniques:
	•	Grid search
	•	Random search
	•	Bayesian optimization


6. Model Validation

- Purpose: Ensure model generalizes to unseen data.
- Techniques:
	•	Hold-out validation set testing
	•	Cross-validation with unseen folds
	•	Testing on entirely separate datasets if available


7. Interpretability and Insight Generation

- Purpose: Understand why the model makes certain predictions to communicate insights to stakeholders.
- Techniques:
	•	Feature importance plots
	•	SHAP or LIME for complex models
	•	Partial dependence plots

 ### feature engineering over food categories 

 Categories:

1. Fast Food / Chain Restaurants

✅ Features 

	•	Visit frequency: number of purchases per week/month at fast food chains
	•	Average spend per visit: total spend / number of visits
	•	Time of day: categorize transactions as breakfast, lunch, dinner, late night
	•	Brand loyalty indicator: % of fast food spend at a single chain vs multiple chains


2. Coffee

✅ Features 

	•	Daily coffee spend: average spend per coffee purchase day
	•	Morning routine indicator: % of coffee purchases before 10 AM
	•	Chain vs independent: binary flag for Starbucks/Peet’s vs local cafés
	•	Coffee purchase frequency tier: low (1-2/week), medium (3-5/week), high (daily)


3. Grocery

✅ Features 

	•	Weekly grocery budget: total grocery spend divided by number of weeks
	•	Store type indicator: grocery chain (e.g. Safeway) vs specialty (Whole Foods, Trader Joe’s)
	•	Basket size category: small (<$20), medium ($20-$100), large (>$100)
	•	Purchase frequency tier: low (1-2/month), medium (weekly), high (multiple per week)


4. Meal Kits

✅ Features 

	•	Subscription status indicator: binary flag if user subscribes to meal kits
	•	Spend per kit: average transaction value for meal kit purchases
	•	Meal kit frequency: number of meal kit purchases per month
	•	Share of food budget: % of total food spend allocated to meal kits


5. Delivery

✅ Features 

	•	Delivery spend per order: average delivery transaction amount
	•	Delivery frequency: number of delivery orders per week/month
	•	Late-night delivery indicator: % of delivery orders after 9 PM
	•	Platform loyalty: % of orders from single platform (Uber Eats vs DoorDash)


Cross-cutting features (frequency, budget, tier)

Across all categories, you probably built:

	•	Spending tiers: group users into low, medium, high spenders per category
	•	Frequency tiers: segment users by how often they transact in each category
	•	Budget share features: % of overall budget spent per category (e.g. coffee spend as % of total food spend)
	•	Recency features: days since last transaction in each category
	•	Time-based patterns: weekday vs weekend spending, or time-of-day trends

 ### machine learning model readiness

 What is “model readiness”?

In data science, model readiness means:

✔️ Preparing data so it can be effectively used by machine learning algorithms to learn patterns and make accurate predictions.

It involves cleaning, transforming, and structuring data to maximize model performance.

How did your feature engineering work contribute to model readiness?

When you engineered features from transactional data, you:

✅ Transformed raw transactions into meaningful inputs.

For example:

	•	Instead of just having raw purchase amounts, you created:
	•	Average spend per visit
	•	Visit frequency
	•	Spending tiers

✅ Encoded behavioral patterns as numeric features.

Models can’t understand text labels like “high spender” unless encoded as a category or numeric tier.

✅ Created features with predictive power.

For example:

	•	Morning coffee routine indicator could predict user churn for a coffee chain.
	•	Delivery frequency could predict likelihood to subscribe to a meal kit.

✅ Handled data types and distributions.
Ensuring features were scaled or encoded properly, e.g.:

	•	Standardizing continuous features (mean=0, std=1) for models like logistic regression.
	•	One-hot encoding categorical variables for tree-based models.

✅ Reduced data sparsity and noise.

By aggregating individual transactions into user-level features, you created structured, condensed datasets suitable for modeling.

Why is this important for machine learning?

🔑 Good features = better model performance.

Models rely on features that capture real, relevant patterns in user behavior. Raw data often lacks that structure.

