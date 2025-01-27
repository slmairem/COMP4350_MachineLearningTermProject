# COMP4350_MachineLearningTermProject

### Project Overview
**Airport Flight Delay Prediction**
- **Introduction:** Predicts how much a flight will be delayed at an airport.
- **Features:** Flight Distance, Weather Conditions, Flight date(Month, DayofMonth, DayofWeek), Departure Delay
- **Label:** Delay time (Continuous value)

### Feature Engineering
**1. Handling Continuous Features:** 
- **DepDelay (Departure Delay):** This feature is directly used without transformation in the code. However, any missing values in the **DepDelay** column are handled by **converting to numeric and removing rows with NaN** values.
- **Distance (Flight Distance):** Like DepDelay, Distance was scaled to align with other numerical variables and ensure compatibility with regression models

**2. Encoding Categorical Features:**
- **WeatherCondition:** The WeatherCondition feature, which was derived based on the Month of the flight, was encoded using one-hot encoding. Categories like "Snowy," "Rainy," "Cloudy," and "Sunny" were transformed into numerical features.

 **3. Target Variable**
 - **ArrDelay (Arrival Delay):**  Any NaN values in ArrDelay were removed during the data cleaning process.

 ### Algorithms and Performance Metrics
- Comparing different regression models, including **Linear Regression** and **Random Forest Regressor**.
-  The evaluation is based on performance metrics such as **Mean Absolute Error (MAE)**, **Mean Squared Error (MSE)**, and **R² score**.

### Dataset
The dataset used for the Airport Flight Delay Prediction problem consists of the following columns:
- **DepDelay:** Departure delay (in minutes, continuous value).
- **Distance:** Flight distance (in miles, continuous value).
- **Month:** The month in which the flight occurred (1 for January, 7 for July).
- **DayofMonth:** The day of the month (a value between 1 and 31).
- **DayOfWeek:** The day of the week (1 for Monday, 7 for Sunday).
- **WeatherCondition:** Weather condition (a categorical variable such as "Snowy", "Rainy", "Sunny").
- **ArrDelay:** The continuous target variable representing the arrival delay of the flight in minutes.

The dataset has been processed and split into three subsets:
- **Training set (60%):** Used for training the machine learning model.
- **Validation set (20%):** Used to fine-tune the model and evaluate performance during training.
- **Test set (20%):** Reserved for the final evaluation of the model.

## Notes
- **Source of Dataset:** The original dataset, **Combined_Flights_2022.csv**, is sourced from Kaggle and covers data for the first seven months of 2022. You can access the dataset from the following link: https://www.kaggle.com/datasets/sriharshaeedala/airline-delay/data
- The dataset used in this project is sampled_data_with_weatherCond.csv, which includes the weather condition data added in Step 2.
- The process should **start from Step 3: Feature Engineering and Data Splitting**, after importing the .csv file, as the data has already been preprocessed and saved in the **sampled_data_with_weatherCond.csv** file.
