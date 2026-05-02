Crime & Housing Data Analysis (New Jersey)

Project Overview
This project analyzes the relationship between crime statistics and housing characteristics across municipalities in New Jersey. The goal is to determine how crime and housing features influence **median rent prices** and **median home values**, and to extract meaningful, actionable insights for urban planning.
---
Objectives
- Explore how crime rates affect housing prices and rent
- Identify the most important features influencing property value
- Validate assumptions using statistical hypothesis testing
- Build predictive models for housing values
- Provide actionable insights based on findings
---
Datasets Used
1. FBI Crime Data
- Source: FBI Crime Statistics (New Jersey)
- Features: violent crime, burglary, robbery, etc.
2. U.S. Census Bureau Housing Data
- Source: Census Bureau Housing Characteristics
- Features: median house value, rent, number of rooms, household size, etc.
---
Data Preprocessing
- Removed metadata and irrelevant rows/columns
- Cleaned column names and standardized formatting
- Dropped redundant and leakage-prone features (e.g., SMOC)
- Converted string values to numeric
- Merged datasets on city/municipality
- Normalized crime counts into **rates per 1,000 people**
---
Exploratory Data Analysis (EDA)
Feature Distributions
- Rent prices were **right-skewed**, indicating a small number of high-rent outliers
- House values were **left-skewed**, showing concentration in higher-value homes
**Impact:** Skewness suggests potential outliers, which can affect model accuracy
---
Correlation Analysis
- Strong correlations found between:
  - Median rent ↔ Median house value
  - Median rooms ↔ House value
- Evidence of **multicollinearity** among housing features
**Action:** Reduced features to top 15 most correlated variables
---
Bivariate Analysis
- Weak relationship between population and house value
- Slight negative relationship between rent and violent crime
---
Hypothesis Testing
Hypothesis:
- **H0:** Crime rates do not significantly affect rent or house values  
- **H1:** Crime rates significantly affect rent or house values  
Method:
- Ordinary Least Squares (OLS) Regression
Results:
- Rent Model:
  - R² ≈ 0.49
  - p-value < 0.05 → Reject H0
- House Model:
  - R² ≈ 0.63
  - Crime variables were **not statistically significant**
Conclusion:
- Some crime variables impact rent
- Crime has **little to no significant effect on house value**
---
Model Building
Model Used:
- Random Forest Regression
Target:
- Median House Value
Evaluation Metrics:
- RMSE (Root Mean Squared Error)
- R² Score
Results:
- RMSE: *[INSERT YOUR VALUE]*
- R²: *[INSERT YOUR VALUE]*
---
Feature Importance
Top predictors of house value:
- Median number of rooms
- Median rent
- Household size
Crime-related features ranked significantly lower.
—
Key Insights (The "Aha!" Moment)
- Housing characteristics are **far more important** than crime in determining property value
- Crime has **more influence on rent** than on home value
- High-value housing areas are not necessarily low-crime areas
---
Actionable Insight
Urban policy should prioritize:
- Improving housing quality (e.g., space, infrastructure)
- Expanding residential development
Rather than focusing solely on crime reduction when aiming to increase property values.
******
