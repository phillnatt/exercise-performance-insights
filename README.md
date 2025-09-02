# Predictive Modelling & Behavioural Insights from Exercise Performance Data

## Executive Summary

This project investigates behavioural patterns in exercise performance using a publicly available dataset. The primary objective is to develop predictive models that estimate calories burned and assess weight goal achievement based on physiological and behavioural features. The analysis integrates core data science practices including data engineering, exploratory analysis, machine learning modelling, and stakeholder-focused visualisation.

---

## Tools & Infrastructure

- **Programming Environment**: Google Colab (Python)
- **Libraries Used**:
  - `pandas` for data manipulation
  - `scikit-learn` for machine learning models
  - `seaborn` and `matplotlib` for visualisation
- **Dashboarding**: Power BI for interactive stakeholder reporting
- **Version Control**: GitHub for reproducibility and collaboration

---

## Data Engineering

The dataset was cleaned and transformed to support effective analysis. Key engineering steps included:

- **Feature Creation**:
  - `Weight_Diff`: Difference between dream weight and actual weight
  - `Age_Group`: Binned age categories (18–30, 31–45, 46–60)
  - `Intensity_Level`: Categorical encoding of exercise intensity (Low, Medium, High)

- **Encoding**:
  - Categorical variables such as gender, weather, and exercise type were encoded using `LabelEncoder`.

- **ETL Pipeline**:
  - Structured data preparation steps were implemented to ensure consistency and readiness for modelling.

---

## Data Analytics

The analysis applied multiple modelling techniques to explore relationships and predict outcomes:

- **Exploratory Data Analysis (EDA)**:
  - Histograms to assess distribution of calories burned
    
  ![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/a71109f914a3c4abc9860b1e78440a832ec1b30a/02%20Images/calorie_burn_by_exercise.png)
  
  - Boxplots to compare gender-based performance
    
  ![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/a71109f914a3c4abc9860b1e78440a832ec1b30a/02%20Images/Calories_burned_gender.png)
  
  - Correlation heatmaps to identify feature relationships
    
  ![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/a71109f914a3c4abc9860b1e78440a832ec1b30a/02%20Images/correlation_heatmap.png)

- **Regression Modelling**:
  - Used to predict calories burned based on physiological features
  - Model performance: RMSE = 117.7, R² = -0.048
  - Interpretation: Low predictive power
  ![alt image](https://github.com/phillnatt/exercise-performance-insights/blob/5d7586acb64b77aeacd7eec4ee6b6eb8d70bba9d/02%20Images/Rnumber.png)
  - This is likely due to missing contextual factors such as diet, metabolism and exercise consistency.


- **Classification Modelling**:
  - Logistic regression to classify weight goal achievement
  ![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/0615cf5f287337e25e4ff4200a9773fd5120ce2c/02%20Images/Classification_matrix.png)
  - ![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/0615cf5f287337e25e4ff4200a9773fd5120ce2c/02%20Images/confusion_matrix.png)
  - Accuracy: ~51%, indicating poor class separation
  - This low accuracy indicates that goal achievement is incredibly complex and requires the analysis of additional factors not available within this dataset
  

- **Clustering**:
  - K-Means clustering revealed three distinct behavioural groups based on exercise intensity, duration, and calories burned
![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/main/02%20Images/K_Means_Clustering.png)
  - Whilst the clustering revealed some groupings within the data, they were not strongly separated within the results, meaning that whilst they were useful for exploratory purposes they are not definitive without further data validation and investigation. 
---

## Visualisation

Visualisation played a key role in communicating insights:

- **Static Visuals**:
  - Plots generated during EDA are stored in the `images/` folder

- **Interactive Dashboard**:
  - Power BI dashboard allows filtering by age group, gender, and exercise type
![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/0615cf5f287337e25e4ff4200a9773fd5120ce2c/03%20Dashboard/Dashboard1_Overview.png)
  - Overview screen showing highlights of data, including gender split, users average BMI & Weight, and average calories burned per session
    
![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/0615cf5f287337e25e4ff4200a9773fd5120ce2c/03%20Dashboard/Dashboard2_Performance_insights.png)
  - Key performance insights section showing performance indicators such as average heart rate and calories burned over time
  - 
![image alt](https://github.com/phillnatt/exercise-performance-insights/blob/0615cf5f287337e25e4ff4200a9773fd5120ce2c/03%20Dashboard/Dashboard3_Environmental_Factors.png)
  - Section showing how weather conditions impact performance, using key veriables such as calories burned, intensity level, and average duration

---

## Key Learnings

- Predictive accuracy is limited without contextual behavioural data (e.g., diet, sleep, motivation): While exercise metrics like duration, heart rate, and intensity offer valuable insights, they do not fully explain performance outcomes or behavioural trends. Factors such as sleep quality, dietary habits, stress levels, and motivation play a critical role in shaping physical performance. Without these contextual variables, the model's ability to generalize or explain variance is inherently constrained.
- Visualisation enhances stakeholder engagement and supports decision-making: Data visualisations—such as histograms, boxplots, and heatmaps—were instrumental in communicating findings to non-technical stakeholders. They helped surface trends, outliers, and relationships in an intuitive format, making it easier to align decisions with evidence. Visual tools also foster transparency and trust in the modelling process.

---

## Recommendations

To improve future iterations of this project:

- **Data Enrichment**:
  - To improve the explanatory power and robustness of future models, it is recommended to incorporate behavioural and lifestyle variables. These may include:
        - Dietary intake (e.g., macronutrient balance, hydration)
        - Sleep quality and duration
        - Mental health indicators (e.g., stress, motivation, mood)
        - Additional environmental factors (e.g., area, time of day)

- **Advanced Modelling**:
  - Explore time-series analysis for longitudinal tracking
        -  Implement models that account for temporal dependencies, enabling longitudinal tracking of performance trends and behavioural changes.
  - Use model interpretability tools to explain predictions
        - Use tools such as SHAP (SHapley Additive exPlanations) or LIME (Local Interpretable Model-Agnostic Explanations) to explain individual predictions and uncover feature importance, which is crucial for transparency and trust.

- **Mixed Methods**:
  - Quantitative metrics alone may not capture the full picture. Combining them with qualitative feedback—such as user interviews, surveys, or diary entries—can:
      - Reveal underlying motivations and barriers
      - Validate model outputs against lived experiences
      - Provide richer, more actionable insights for intervention design

---
