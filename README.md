## Solar Radiation Prediction

### Project Overview

This project aims to predict **solar radiation levels** based on various environmental and atmospheric factors. By analyzing features such as temperature, pressure, humidity, wind direction and speed, and time-based metrics, the goal is to develop a regression model that can accurately forecast solar radiation. This is a crucial task for solar energy systems, weather forecasting, and agricultural planning.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - SolarEnergy](https://www.kaggle.com/datasets/dronio/SolarEnergy)
  * **Size**: 32,686 entries, 11 columns
  * **Key Features**:
      * `Temperature`, `Pressure`, `Humidity`, `WindDirection(Degrees)`, `Speed`.
      * **Time-based Features**: `Time_Hour`, `Time_Minute`, `Time_Second`, `SunriseHour`, `SunriseMinute`, `SunsetHour`, `SunsetMinute`.
  * **Approach**:
      * **Data Cleaning**: The `Data`, `Time`, `TimeSunRise`, and `TimeSunSet` columns were used to engineer new time-based features and then dropped.
      * **Exploratory Data Analysis**: A variety of visualizations, including line plots, histograms, box plots, and a pairplot, were used to analyze data distributions and feature relationships. A bar chart of average radiation by hour highlighted a clear temporal pattern.
      * **Regression Task**: The target variable is `Radiation`.
      * **Models Used**:
          * A suite of regression models were trained, including Ridge, XGBoost, Random Forest, AdaBoost, Gradient Boosting, Bagging, Decision Tree, SVR, and K-Nearest Neighbors (KNN).
  * **Best R² Score**:
      * **0.944** with KNN Regressor.
      * **0.943** with Random Forest Regressor.
      * **0.933** with Bagging Regressor.
      * The high R² scores indicate that the models are highly effective at predicting solar radiation based on the combination of atmospheric conditions and time-based features.

-----

### Purpose and Applications

  * **Solar Energy Forecasting**: Enables accurate prediction of solar power generation for energy grid management.
  * **Agricultural Planning**: Assists farmers in optimizing planting and irrigation schedules based on expected solar radiation.
  * **Weather Forecasting**: Provides a foundational model for more complex meteorological analysis.
  * **Environmental Monitoring**: Supports research on the effects of solar radiation on environmental systems.

-----

### Installation

Clone the repository and extract the data from the zip file.

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Performing comprehensive hyperparameter tuning for the top-performing regression models.
  * Investigating the impact of the data cleaning and feature engineering steps, and trying alternative methods.
  * Exploring more advanced time-series forecasting techniques that can capture temporal dependencies.
  * Adding explainability (e.g., SHAP or LIME) to understand which factors are the most significant drivers of solar radiation.
