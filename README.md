# 🚙 Ford Car Price Prediction

## 📌 Project Overview
This project implements a Machine Learning model to predict the resale price of used Ford cars. By analyzing various vehicle attributes, the model estimates market value, achieving an accuracy of approximately **84.6%**.

## 📂 Dataset
The model is trained on the `ford.csv` dataset, containing the following features:
- **Categorical:** `model`, `transmission`, `fuelType`
- **Numerical:** `mileage`, `tax`, `mpg`, `engineSize`
- **Target Variable:** `price`

## 🛠️ Tech Stack
- **Python**
- **Pandas & NumPy** (Data processing)
- **Matplotlib & Seaborn** (Exploratory Data Analysis)
- **Scikit-Learn** (Preprocessing & Model Training)

## ⚙️ Methodology
1. **Feature Engineering:**
   - Created a new feature `car_age` (calculated as `2026 - year`) to better capture vehicle depreciation.
   - Dropped the original `year` column to reduce redundancy.
2. **Exploratory Data Analysis (EDA):**
   - Analyzed correlations using Heatmaps (e.g., Tax vs. Price).
   - Visualized price distributions with Boxplots.
3. **Preprocessing Pipeline:**
   - Implemented a `ColumnTransformer` to handle mixed data types automatically:
     - **MinMaxScaler** applied to numerical columns (`mileage`, `tax`, `mpg`, `engineSize`, `car_age`).
     - **OneHotEncoder** applied to categorical columns (`model`, `transmission`, `fuelType`).
4. **Model Training:**
   - **Algorithm:** Linear Regression
   - **Split:** 80% Training / 20% Testing

## 📊 Results
The model was evaluated using the R² Score metric:
- **Accuracy:** 84.58%
