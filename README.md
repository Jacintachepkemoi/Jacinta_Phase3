# Jacinta_Phase3
Business Understanding
Vaccination stands as one of humanity's greatest achievements in public health, having effectively eradicated or controlled numerous diseases. However, recent years have witnessed a concerning rise in vaccine skepticism, leading to declining immunization rates and outbreaks of preventable diseases. Understanding the factors driving vaccine hesitancy and predicting vaccination uptake is imperative for public health officials and policymakers.

This project leverages data from the National Flu Survey (NHFS 2009) to predict individuals' likelihood of receiving the H1N1 flu vaccine. By examining past vaccination patterns, the study aims to shed light on contemporary vaccination behaviors, particularly pertinent in the context of emerging pandemics like COVID-19.

Problem Statement
Vaccine hesitancy poses a significant challenge to public health efforts, leading to decreased immunization rates and increased vulnerability to infectious diseases. Understanding the factors influencing individuals' decisions regarding vaccine uptake is crucial for designing effective interventions and promoting community immunity. In this context, the project aims to predict the likelihood of individuals receiving the H1N1 flu vaccine using machine learning techniques and data from the National Flu Survey (NHFS 2009).

Objectives
Prediction: Develop machine learning models to predict individuals' H1N1 vaccine uptake based on demographic, socio-economic, and attitudinal factors.

Identify Influential Factors: Determine the most influential factors affecting H1N1 vaccine acceptance, including doctor recommendations, health insurance coverage, perceptions of vaccine effectiveness, and risk perceptions related to H1N1.

Model Evaluation: Assess the performance of different machine learning algorithms, including Decision Tree Classifier, Logistic Regression, Random Forest, K-Nearest Neighborhood Classifier, and Gradient Boosting Classifier, in predicting H1N1 vaccine uptake.

Impact Analysis: Analyze the implications of the predictive models and identify actionable insights for public health professionals and policymakers to improve vaccination rates.



Data Preparation


To address the issue of missing data in the H1N1 Flu Vaccines dataset, I developed a Python class called DataChecker that systematically handles various data preprocessing tasks. The initial steps involved loading the dataset and identifying missing values and duplicate rows. To clean the dataset, I implemented a method to drop specific columns that had a high percentage of missing values, as these columns (namely health_insurance, employment_industry, and employment_occupation) were not deemed essential for analysis.

For the remaining missing data, I took a two-pronged approach. First, I targeted the numeric columns by calculating the mean of each column and replacing the missing values with these means. This approach ensures that the numeric integrity of the data is maintained without introducing biases. For non-numeric columns, I replaced the missing values with the mode, which is the most frequently occurring value in each column. This method preserves the categorical nature of these columns and maintains the consistency of the data.

The DataChecker class included methods for these tasks, ensuring a modular and reusable code structure. After processing, I verified that the dataset had no remaining missing values, achieving a complete and clean dataset ready for further analysis. This comprehensive approach allowed for efficient data preprocessing, handling both numeric and categorical missing values appropriately, thus ensuring the integrity and usability of the dataset for subsequent analyses.


Data Analsis


Modelling

Logistic Regression

The logistic regression feature importance plot provides valuable insights into the factors influencing individuals' decisions to receive the H1N1 vaccine based on the 2009 National H1N1 Flu Survey data. The most significant predictors include recommendations from doctors (num_doctor_recc_h1n1), opinions on the vaccine's effectiveness (num_opinion_h1n1_vacc_effective), and perceived risk of H1N1 (num_opinion_h1n1_risk). These factors likely highlight the importance of trusted medical advice and personal beliefs about the vaccine's benefits and risks in driving vaccination decisions. Conversely, the least significant predictors include behavioral factors like going outside the home (num_behavioral_outside_home), household adults (num_household_adults), and employment status (cat_employment_status_Unemployed). These factors may have lower importance because they do not directly relate to medical opinions or personal health perceptions, which are more immediate concerns when deciding to get vaccinated. Understanding both the most and least influential factors can help public health officials tailor future vaccination campaigns. Emphasizing the importance of doctor recommendations and addressing public concerns about vaccine efficacy and risks can improve vaccine uptake, while recognizing that some demographic and behavioral factors may not significantly impact vaccination decisions.
