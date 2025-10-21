# 🚗 Used Car Price Prediction

## 📘 Overview
This project focuses on predicting the prices of used cars using multiple regression techniques in Python. The objective was to explore how various car attributes—such as horsepower, engine size, and other specifications—affect the overall market price of a vehicle.

Three regression models were implemented:
- **Linear Regression**
- **Multiple Linear Regression**
- **Polynomial Regression**

Each model was evaluated and compared using statistical performance metrics such as **R²** and **Mean Squared Error (MSE)**.

---

## 🧾 Dataset Description
The dataset used in this project contains several attributes related to used cars, such as their technical specifications and physical characteristics.  
Some key features include:

- `symboling`
- `normalized-losses`
- `make`
- `fuel-type`
- `aspiration`
- `num-of-doors`
- `body-style`
- `drive-wheels`
- `engine-location`
- `wheel-base`
- `length`, `width`, `height`
- `curb-weight`
- `engine-size`
- `horsepower`
- `peak-rpm`
- `city-mpg`, `highway-mpg`
- `price` *(Target Variable)*

---

## 🧹 Data Cleaning and Preprocessing

### 🧩 Steps Performed
1. **Handling Missing Values:**  
   Missing numerical data was filled using mean or median values.  
   Categorical missing values were handled appropriately using imputation or removal.

2. **Encoding Categorical Variables:**  
   String-based columns such as `make`, `fuel-type`, and `body-style` were converted into numerical labels using Label Encoding.

3. **Feature Selection and Preparation:**  
   Relevant numerical features like `engine-size`, `horsepower`, and `curb-weight` were selected for modeling.

4. **Data Normalization:**  
   Features were scaled where necessary to maintain consistency across units and ranges.

5. **Splitting Data:**  
   The dataset was divided into independent variables (`X`) and dependent variable (`y`), and further split into training and testing sets using an 90/10 ratio.

---

## 🧠 Model Implementation

### 1️⃣ Linear Regression
A **simple linear regression** model was trained using one independent variable (e.g., horsepower) to predict car prices.  
This model provided a baseline understanding of how a single factor influences price.

---

### 2️⃣ Multiple Linear Regression
A **multiple linear regression** model was developed using several numerical predictors such as `engine-size`, `curb-weight`, and `horsepower`.  
This model improved predictive accuracy by considering multiple relationships simultaneously.

---

### 3️⃣ Polynomial Regression
To capture non-linear patterns between features and price, **Polynomial Regression** was applied.  
Different polynomial degrees were tested, and the one with the best performance (highest R², lowest MSE) was selected.

---

## 📊 Model Evaluation

Each model was evaluated using **R² (coefficient of determination)** and **Mean Squared Error (MSE)**.

| Model Type | R² Score | Mean Squared Error (MSE) |
|-------------|-----------|--------------------------|
| Linear Regression | ~0.80 | ~31,755,395 |
| Multiple Linear Regression | ~0.84 | ~12,036,316 |
| Polynomial Regression | ~0.85–0.86 | Lowest among all |

### ✅ Interpretation:
- A higher **R²** indicates a better fit of the model to the data.  
- A lower **MSE** represents more accurate predictions.  
- **Polynomial Regression** performed the best, capturing more complex relationships within the data.

---

## 📈 Visualizations

Two key plots were generated to visualize model accuracy:

1. **Actual vs Predicted Values (Linear Regression):**  
   - Displays how closely predicted prices follow actual prices.
   - The plot shows a generally linear upward trend, but with deviations at higher prices.

2. **Actual vs Predicted Values (Polynomial Regression):**  
   - The predicted curve closely follows the actual data points.
   - Indicates that polynomial regression captures non-linear relationships better.

---

## 🧩 Conclusion

- Linear Regression gave an initial estimate of the price trend based on a single feature.  
- Multiple Linear Regression improved performance by considering multiple predictors.  
- Polynomial Regression achieved the **best performance** overall, providing the highest accuracy and lowest error.  

Hence, **Polynomial Regression** is the most suitable model for predicting used car prices in this dataset.

---

## 🔮 Future Improvements

For further improvement and exploration, the following steps can be added:
- Apply **Ridge** or **Lasso Regression** for regularization and overfitting control.
- Use **K-Fold Cross-Validation** for more robust accuracy estimation.
- Implement **feature importance analysis** to identify key predictors of car price.

---

## 🧰 Technologies Used
- **Python 3**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Scikit-learn**
- **Jupyter Notebook**
