# Position Salary Prediction using Random Forest Regression

This project demonstrates how to use a **Random Forest Regression** model to predict employee salaries based on their position level. It includes model training, prediction, and visualization.

---

## 📁 Dataset

The dataset used is `Position_Salaries.csv`, which contains:

- **Position Title** (not used directly in the model)
- **Level** (used as the input feature `X`)
- **Salary** (used as the target variable `y`)

Example structure:

| Position       | Level | Salary     |
|----------------|-------|------------|
| Business Analyst | 1   | 45000      |
| CEO            | 10    | 1000000    |

---

## 🚀 Workflow

1. **Import Libraries**  
   Uses Python's scientific stack: `NumPy`, `Pandas`, `Matplotlib`, and `scikit-learn`.

2. **Load Dataset**  
   Extracts the `Level` column as the feature `X` and the `Salary` column as the target `y`.

3. **Train the Model**  
   Trains a `RandomForestRegressor` with 10 decision trees (`n_estimators=10`) on the full dataset.

4. **Predict a New Result**  
   Predicts the salary for a position level of `6.5`.

5. **Visualize the Results**  
   - Plots the original data points (red).
   - Shows the model’s predictions (blue curve) over a high-resolution grid to illustrate the stepwise nature of the predictions.

---

## 📈 Why the Graph Looks Stepwise

Random Forest Regression is an **ensemble method** that averages predictions from multiple decision trees. Each tree splits data into regions and outputs constant predictions for each. The result is a **stepwise plot**, especially noticeable when:

- The number of trees is relatively low (`n_estimators=10`).
- Only **one independent variable** is used (in this case, `Level`), so the model lacks the complexity that additional features might provide for smoother prediction curves.

---

## 🛠️ Requirements

- Python 3.x
- numpy
- pandas
- matplotlib
- scikit-learn

Install required packages with:

```bash
pip install numpy pandas matplotlib scikit-learn
