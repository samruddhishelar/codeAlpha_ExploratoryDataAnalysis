~~Titanic Dataset — Exploratory Data Analysis

Exploratory Data Analysis (EDA) on the Titanic passenger dataset, done as Task 2 of the CodeAlpha Data analytics Internship.

Objective

Understand the structure of the Titanic dataset, find real patterns in who survived, and validate those patterns statistically — before any modeling.

Questions Asked :-
1. Did passengers under 18 survive more than passengers 18 and older?

2. Who survived more — male or female passengers?

3. Did 1st class passengers survive more than 3rd class passengers?

Data :-
Source: Kaggle Titanic dataset
891 passenger records, 12 columns (Survived, Pclass, Sex, Age, SibSp, Parch, Fare, Embarked, etc.)

Key Findings :-
Question                    	       Result	                           Statistically Significant?
Male vs. female survival	        74.2% (female) vs. 18.9% (male)	        Yes (p ≈ 1.2×10⁻⁵⁸)
1st class vs. 3rd class survival	63.0% (1st) vs. 24.2% (3rd)	            Yes (p ≈ 4.5×10⁻²³)
Under 18 vs. 18+ survival	        53.9% (under 18) vs. 36.1% (18+)	    Yes (p ≈ 0.00039)

Summary: Sex had the strongest effect on survival, followed by passenger class, and then age group. All three relationships were confirmed with chi-square tests (p < 0.05), meaning they're real patterns and not random chance.

Data Quality Issues Found :-
Age: ~20% missing — needs imputation before modeling.
Cabin: ~77% missing — excluded from analysis.
Embarked: 2 missing values — minor, safe to fill with the mode.
Fare: right-skewed with outliers — worth a closer look or log transform.
Project Files
titanic_eda.ipynb — full analysis notebook (code, charts, statistical tests)
titanic_eda_report.docx — written report with findings and visualizations
titanic.csv — dataset used

Tools Used :-
Python, pandas, matplotlib, seaborn, scipy (chi-square tests)