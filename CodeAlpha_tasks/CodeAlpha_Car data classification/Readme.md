# codealpha_tasks

Hey everyone! This is my final submission project for my Machine Learning course. In this project, I have built a predictive model that estimates the selling price of used cars based on several factors like its original showroom price, age, kilometers driven, fuel type, and transmission.

I used a **Random Forest Regressor** for this project because it gave me much better accuracy compared to basic Linear Regression during my initial testing.

---

## 📊 Dataset Description

The dataset used is `car data.csv` which I loaded into Pandas. It contains 301 entries with the following details:
* **Car_Name**: Brand/Model of the car (dropped during preprocessing due to high variety).
* **Year**: The year the car was bought.
* **Selling_Price**: The price the car is being sold for (This is our **Target Variable**).
* **Present_Price**: The original showroom price of the car when it was new.
* **Driven_kms**: Total kilometers the car has been driven.
* **Fuel_Type**: Petrol / Diesel / CNG.
* **Selling_type**: Dealer / Individual seller.
* **Transmission**: Manual / Automatic.
* **Owner**: Number of previous owners.

---

## 🛠️ Step-by-Step Workflow

### 1. Data Cleaning & Feature Engineering
* Checked for missing/null values using `df.isnull().sum()`. Luckily, the dataset was completely clean.
* **Feature Engineering**: Instead of using the raw `Year` column directly, I created a new feature called `Car_Age` (`2026 - df['Year']`). This helps the model calculate depreciation much better since a car's value drops as it gets older.
* Dropped the `Car_Name` and the old `Year` column to keep things simple and prevent overfitting.

### 2. Categorical Data Encoding
* Since machine learning algorithms can't read text values like "Petrol" or "Manual", I used **One-Hot Encoding** (`pd.get_dummies(..., drop_first=True)`) to convert columns like `Fuel_Type`, `Selling_type`, and `Transmission` into numerical binary vectors (0s and 1s).

### 3. Model Training
* Split the processed dataset into an **80% Training set** and a **20% Test set** using `train_test_split` with `random_state=42` to keep my splits consistent every time I rerun the script.
* Initialized the `RandomForestRegressor` with 100 estimators and fit it onto the training data.

---

## 📈 Model Performance & Results

After evaluating the model on the unseen test dataset, these are the scores I achieved:

* **Mean Absolute Error (MAE):** `0.64` (On average, my model's predictions are only off by around 0.64 units/Lakhs!)
* **Mean Squared Error (MSE):** `0.93`
* **R-squared ($R^2$) Score:** `0.9595` 
  > **What this means:** My model is able to explain **95.9% of the variance** in the used car prices. It's highly accurate!

### 🔍 Feature Importance (What matters most?)
According to the model's feature importance analysis, here is what affects a car's resale value the most:
1. **Present Price (Showroom Price):** ~88% impact (The original cost is the biggest anchor).
2. **Car Age:** ~5.9% impact (Depreciation over time).
3. **Kilometers Driven:** ~4% impact (Wear and tear).

---

## 🚀 How to Run the Code on Your Machine

1. **Clone the repo or download the files** (`car data.csv` and the Python script).
2. **Install the required libraries** if you haven't already: