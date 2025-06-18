# Car Insurance Risk & Profitability Analytics

This project is part of my work at AlphaCare Insurance Solutions to analyze historical car insurance claims data in South Africa and develop predictive models for risk assessment and marketing strategy optimization.

Task 1: Exploratory Data Analysis (EDA) & Statistical Profiling
Goal: Gain insight into customer behavior and claim trends.

Deliverables:
Summary statistics (mean, std, quartiles)

Visuals: heatmaps, bar plots, boxplots

Loss ratio by province

Claim distribution by demographics (gender, bank, language)

Task 2: DVC Setup (Data Version Control)
Goal: Make the data pipeline reproducible using DVC.

Steps:
Initialize DVC:
dvc init

Add raw data to DVC:
dvc add data/raw/MachineLearningRating_v3.txt

Track with Git:

bash
Copy
Edit
git add data/raw/MachineLearningRating_v3.txt.dvc .gitignore
git commit -m "Track raw dataset with DVC"


Share and reproduce pipeline with collaborators using:
dvc pull and dvc repro

Benefits:
Version control for large data files

Seamless team collaboration without data corruption
Task 3: Hypothesis Testing
Goal: Validate business assumptions statistically.

Examples:
Gender vs claim amount: t-test

Vehicle type vs severity: ANOVA

Bank or language vs claim frequency: statistical testing

Metrics:
t-statistics and F-values

p-values (< 0.05 = significant)

Task 4: Risk-Based Modeling & Premium Estimation
A. Claim Severity (Regression)
Models: Linear Regression, Random Forest, XGBoost

Target: TotalClaims

Metrics: RMSE, R²

B. Claim Probability (Classification)
Models: Random Forest, XGBoost

Target: HasClaim

Metrics: Accuracy, F1, ROC-AUC

C. Premium Calculation Formula
Premium=(Probability×Severity)+Loading+Margin
Premium=(Probability×Severity)+Loading+Margin
Loading: 300 ZAR

Profit Margin: 10% of predicted severity

Output: df['PredictedPremium']

D. Interpretability (SHAP)
Explain model predictions

Identify most influential risk features

Used on trained XGBoost model with shap.summary_plot(...)

Tools Used
pandas, scikit-learn, xgboost, shap, matplotlib, seaborn

DVC for data versioning

Jupyter Notebooks

How to Reproduce
bash
Copy
Edit
# Clone repository
git clone <repo_url>

# Install dependencies
pip install -r requirements.txt

# Pull data
dvc pull

# Run the notebook tasks in order
jupyter notebook
 Branch Strategy
Branch	Description
main	Final project version
task-1	EDA and Statistics
task-2	DVC Integration
task-3	Hypothesis Testing
task-4	Risk Models & Premium Pricing

