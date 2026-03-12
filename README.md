# Salary Prediction Using Linear Regression

## Project Overview
This project predicts the **salary of an employee** based on their **years of experience** using **Linear Regression**. It demonstrates the complete machine learning workflow, including **data cleaning, model training, evaluation, visualization, and saving the trained model**.

---

## Dataset
- The dataset contains **employee experience (years)** and **salary**.
- Source: Publicly available salary dataset ([can be replaced with actual source if needed]).

**Sample Data:**

| YearsExperience | Salary  |
|-----------------|--------|
| 1.1             | 39343  |
| 1.3             | 46205  |
| 1.5             | 37731  |

---

## Libraries & Tools Used
- **Python**  
- **pandas** – Data manipulation  
- **NumPy** – Numerical operations  
- **scikit-learn** – Machine Learning algorithms  
- **Matplotlib / Seaborn** – Data visualization  
- **joblib** – Saving trained models  

---

## Project Steps

1. **Data Loading & Exploration**
   - Loaded the dataset using `pandas`
   - Checked for missing values and data types

2. **Data Cleaning**
   - Handled missing values if any
   - Verified dataset for duplicates

3. **Feature & Target Selection**
   - Feature: `YearsExperience`  
   - Target: `Salary`

4. **Train-Test Split**
   - 80% training data  
   - 20% testing data  
   - Used `train_test_split` from scikit-learn

5. **Model Training**
   - Trained a **Linear Regression** model
   - Code snippet:
     ```python
     from sklearn.linear_model import LinearRegression
     model = LinearRegression()
     model.fit(X_train, y_train)
     ```

6. **Predictions & Evaluation**
   - Predicted salaries for the test set
   - Evaluated using:
     - **R² Score**
     - **Mean Squared Error (MSE)**
     - **Root Mean Squared Error (RMSE)**
   - Example output:
     ```
     R² Score: 0.867
     MSE: 3.45e+08
     RMSE: 18566.2
     ```

7. **Visualization**
   - Plotted **Actual vs Predicted salaries**:
     ```python
     import matplotlib.pyplot as plt

     plt.scatter(y_test, predictions)
     plt.xlabel("Actual Salary")
     plt.ylabel("Predicted Salary")
     plt.title("Actual vs Predicted Salary")
     plt.show()
     ```

8. **Model Saving**
   - Saved the trained model using `joblib`:
     ```python
     import joblib
     joblib.dump(model, "salary_prediction_model.pkl")
     ```

9. **Using the Saved Model**
   - Load the model to predict new salaries without retraining:
     ```python
     model = joblib.load("salary_prediction_model.pkl")
     predicted_salary = model.predict([[5]])  # 5 years experience
     print(predicted_salary)
     ```

---

## Project Structure

---

## Skills Learned
- Data Cleaning & Preprocessing  
- Linear Regression Modeling  
- Model Evaluation (R², MSE, RMSE)  
- Data Visualization  
- Model Saving & Reuse  

---

## GitHub Repository
[View the project on GitHub](https://github.com/Prakalp-74/Salary-prediction-ML)

---

## Author
**Prakalp** – AI & Data Science Enthusiast  
