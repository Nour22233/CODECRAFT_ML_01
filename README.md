 🏠 Task 01 - House Price Prediction using Linear Regression

 📌 Description

This project implements a Linear Regression model to predict house prices based on:

- GrLivArea (Above ground living area square footage)
- BedroomAbvGr (Number of bedrooms above ground)
- FullBath (Number of full bathrooms)

---

 🔍 Dataset

- Source: [House Prices - Advanced Regression Techniques | Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data)
- File used: `train.csv`

---

 💻 Steps Performed

1. Imported Libraries
2. Loaded dataset
3. Explored data
   - Checked null values
   - Filled missing values in `LotFrontage` with neighborhood mean
   - Described data & plotted distributions
4. Correlation analysis
   - Plotted heatmaps to find most correlated features with `SalePrice`
5. Feature selection
   - Selected `GrLivArea`, `BedroomAbvGr`, `FullBath` as input features
6. Train-Test Split
7. Built Linear Regression model
8. Evaluated model
   - Calculated MSE, RMSE, and R²
9. Visualized Results
   - Actual vs Predicted scatter plot
   - Residual plot
   - Distribution plot for `SalePrice`
10. Prediction Example
    - Predicted price for a house with 2000 sqft, 3 bedrooms, and 2 bathrooms.

---

 📈 Model Evaluation Metrics

| Metric | Value |
|---|---|
| Mean Squared Error (MSE) | ~ 2,575,756,086.36 |
| Root Mean Squared Error (RMSE) | ~ 50,752.90 |
| R-squared (R²) | ~ 0.63 |

---

 🔬 Model Coefficients

- Intercept: 52,977.04
- GrLivArea: +102.08 ➔ Each additional sqft increases price by ~102 units.
- BedroomAbvGr: -26,637.42 ➔ Each additional bedroom decreases price by ~26,637 units.
- FullBath: +31,112.29 ➔ Each additional full bathroom increases price by ~31,112 units.

---

Libraries Used

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

 📌 Usage

To predict a new house price:

```python
example_house = np.array([[2000, 3, 2]])
predicted_price = model.predict(example_house)
print("Predicted price for the house is:", predicted_price[0])
