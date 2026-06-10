# Future Sales Prediction using Machine Learning

I built this project to analyze how marketing budgets spent across different channels—specifically **TV**, **Radio**, and **Newspaper**—impact overall **Sales**. Using a Multiple Linear Regression model, the goal is to forecast future sales outcomes and help businesses allocate their advertising spend more efficiently.

---

## 📂 Dataset Overview
The project utilizes the `Advertising.csv` dataset, which contains **200 rows** of data with no missing or null values[cite: 1].
* **TV**: Advertising dollars spent on TV ads (in thousands)[cite: 1].
* **Radio**: Advertising dollars spent on Radio ads[cite: 1].
* **Newspaper**: Advertising dollars spent on Newspaper ads[cite: 1].
* **Sales**: Total units sold (the target variable)[cite: 1].

---

## 🛠️ Project Workflow

### 1. Data Exploration & Cleaning
* Checked for missing data points using `df.isnull().sum()` to ensure data integrity[cite: 1].
* Plotted a correlation heatmap to analyze which media channel holds the strongest relationship with sales growth[cite: 1].

### 2. Feature Engineering & Selection
* **Features ($X$):** `TV`, `Radio`, `Newspaper`[cite: 1]
* **Target ($y$):** `Sales`[cite: 1]

### 3. Model Training
* Split the dataset into **80% Training** and **20% Testing** subsets using a fixed `random_state=42` for reproducible results[cite: 1].
* Implemented and trained a **Linear Regression** model using `scikit-learn`[cite: 1].

---

## 📊 Model Evaluation & Results

The model performs exceptionally well on the unseen test data, yielding the following performance metrics[cite: 1]:

* **Mean Squared Error (MSE):** `3.17` (indicating a very low average squared variance in predictions)[cite: 1].
* **R-squared ($R^2$) Score:** `0.8994` (~90%)[cite: 1].
  > **Takeaway:** This means approximately 90% of the variance in sales can be explained by the changes in our advertising budgets across the three channels[cite: 1].

---

## 🔍 Key Insights & Actionable Business Strategy

By looking at the trained model's coefficients, we can extract real-world strategic advice for the marketing team[cite: 1]:
* **TV Coefficient:** `0.0447` — TV spend drives consistent, steady sales growth[cite: 1].
* **Radio Coefficient:** `0.1892` — Dollar-for-dollar, Radio advertising has the highest individual impact on sales[cite: 1].
* **Newspaper Coefficient:** `0.0028` — The impact is virtually flat, meaning budget increases here don't translate to meaningful sales gains[cite: 1].

💡 **Strategic Recommendations:**
1. **Prioritize Radio and TV:** Focus the majority of the marketing capital on Radio (for maximum ROI per dollar) and TV (for overall volume scaling)[cite: 1].
2. **Minimize Newspaper Spend:** Reallocate the current newspaper ad budget over to TV or Radio, as newspaper ads are currently underperforming and draining resources without driving growth[cite: 1].

---

## 🚀 How to Run This Project

1. **Install Dependencies:**
```bash
   pip install pandas numpy scikit-learn matplotlib seaborn