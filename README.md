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
  - Boxplots to compare gender-based performance
  - Correlation heatmaps to identify feature relationships

- **Regression Modelling**:
  - Used to predict calories burned based on physiological features
  - Model performance: RMSE = 117.7, R² = -0.048
  - Interpretation: Low predictive power due to missing behavioural/contextual variables
- **Classification Modelling**:
  - Logistic regression to classify weight goal achievement
  - Accuracy: ~51%, indicating poor class separation and complexity of behavioural outcomes

- **Clustering**:
  - K-Means clustering revealed three distinct behavioural groups based on exercise intensity, duration, and calories burned

---

## Visualisation

Visualisation played a key role in communicating insights:

- **Static Visuals**:
  - Plots generated during EDA are stored in the `images/` folder

- **Interactive Dashboard**:
  - Power BI dashboard allows filtering by age group, gender, and exercise type
  - Screenshots are available in the `dashboard/` folder

---

## Key Learnings

- Feature engineering significantly influences model performance
- Predictive accuracy is limited without contextual behavioural data (e.g., diet, sleep, motivation)
- Visualisation enhances stakeholder engagement and supports decision-making

---

## Recommendations

To improve future iterations of this project:

- **Data Enrichment**:
  - Incorporate behavioural and lifestyle variables such as diet, sleep quality, and motivation levels

- **Advanced Modelling**:
  - Explore time-series analysis for longitudinal tracking
  - Use model interpretability tools to explain predictions

- **Mixed Methods**:
  - Combine quantitative metrics with qualitative feedback to provide richer insights

---
