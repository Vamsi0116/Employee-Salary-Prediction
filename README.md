# Employee Salary Prediction using Machine Learning

## 📝 Overview

This project demonstrates a complete machine learning workflow to predict employee salaries based on various demographic and professional factors. The goal is to build an accurate regression model by cleaning the data, engineering relevant features, and comparing the performance of several popular algorithms. The final model identifies the XGBoost Regressor as the most effective for this dataset.

---

## ✨ Features

* **Data Cleaning:** Handles missing values, duplicates, and illogical data entries.
* **Exploratory Data Analysis (EDA):** Includes visualizations to understand the relationships between different features and salary.
* **Feature Engineering:** Creates new predictive features, such as:
    * `Experience_Level` (Entry-level, Mid-level, Senior-level, etc.)
    * `Job_Education` (An interaction feature combining job title and education)
    * `Years_of_Experience_sq` (A polynomial feature to capture non-linear trends)
* **Comparative Model Analysis:** Trains and evaluates four different regression models:
    * Linear Regression
    * Decision Tree Regressor
    * Random Forest Regressor
    * XGBoost Regressor
* **Model Evaluation:** Uses standard regression metrics (R-squared, MAE, and RMSE) to assess and compare model performance.

---

## 📊 Dataset

The dataset used for this project is `Salary Data.csv`. It contains the following columns:
* `Age`
* `Gender`
* `Education Level`
* `Job Title`
* `Years of Experience`
* `Salary` (Target Variable)

---

## 🛠️ Installation & Setup

To run this project on your local machine, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required libraries:**
    Create a file named `requirements.txt` and add the following library names to it:
    ```
    pandas
    numpy
    scikit-learn
    xgboost
    matplotlib
    seaborn
    plotly
    joblib
    ```
    Then, run the following command to install them:
    ```bash
    pip install -r requirements.txt
    ```

---

## 🚀 Usage

1.  Launch the Jupyter Notebook environment:
    ```bash
    jupyter notebook
    ```
2.  Open the `EmployeeSalaryPrediction by vamsi.ipynb` notebook.
3.  Run the cells in order from top to bottom to see the entire process from data loading to model evaluation.

---

## 📈 Model Performance

The performance of the trained models was evaluated on the test set. The XGBoost Regressor provided the best results across all key metrics.

| Model                     | R-squared | Mean Absolute Error (MAE) | Root Mean Squared Error (RMSE) |
| ------------------------- | :-------: | :-----------------------: | :----------------------------: |
| **XGBoost Regressor** | **0.8873**| **$10,157.86** | **$14,591.69** |
| Random Forest Regressor   | 0.8778    | $10,437.33                | $15,194.73                     |
| Linear Regression         | 0.8706    | $12,551.78                | $15,640.46                     |
| Decision Tree Regressor   | 0.7938    | $13,000.00                | $19,738.68                     |

---

## 🔮 Future Scope

* **Hyperparameter Tuning:** Fine-tune the XGBoost Regressor's parameters to potentially improve its accuracy further.
* **Feature Management:** Group rare job titles into an 'Other' category to reduce dimensionality and help the model generalize better.
* **Deployment:** Build a simple web application using a framework like Flask or Streamlit to provide salary estimates through a user-friendly interface.
