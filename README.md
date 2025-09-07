# Medical Insurance Cost Prediction 🩺💸

## Introduction
This project aims to predict medical insurance costs for individuals based on a number of personal attributes. By analyzing factors such as age, BMI, smoking habits, and region, we build several regression models to estimate potential insurance charges. This type of prediction is crucial for insurance companies to determine premium costs and for individuals to understand the factors that significantly impact their health expenses.

---

## Dataset
The dataset used is `insurance.csv`, which contains 1,338 rows of data with the following columns:

* **age**: Age of the primary beneficiary.
* **sex**: Gender of the primary beneficiary (male/female).
* **bmi**: Body mass index, providing an understanding of body weight relative to height.
* **children**: Number of children covered by health insurance / Number of dependents.
* **smoker**: Whether the person smokes or not (yes/no).
* **region**: The beneficiary's residential area in the US (northeast, southeast, southwest, northwest).
* **charges**: Individual medical costs billed by health insurance (this is our target variable).

---

## Project Workflow
The project follows a standard data science workflow:
1.  **Data Loading & Initial Exploration**: The dataset is loaded, and we perform an initial inspection of its structure and content.
2.  **Data Cleaning & Preprocessing**: We check for missing values and convert categorical features (like 'sex', 'smoker', and 'region') into a numerical format using one-hot encoding.
3.  **Exploratory Data Analysis (EDA)**: We create visualizations to understand the relationships between different features and the target variable (`charges`).
4.  **Model Building**: The data is split into training and testing sets. Four different regression models are trained:
    * Linear Regression
    * Ridge Regression
    * Random Forest Regressor
    * Gradient Boosting Regressor
5.  **Model Evaluation**: The models are evaluated on the test set using metrics like R-squared, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE) to determine the best-performing model.

---

## Key Insights from EDA
* **Smoking is the Strongest Predictor**: The analysis clearly shows that smokers have significantly higher medical charges than non-smokers.
* **Age and BMI are Significant Factors**: Medical costs tend to increase with both age and BMI.
* **Skewed Distribution**: The distribution of charges is heavily skewed, with most individuals having low costs and a smaller number having very high costs.

---

## Modeling Results
The performance of the trained models was compared, and the **Gradient Boosting Regressor** emerged as the top performer.

| Model               | R-squared | MAE         | RMSE        |
|---------------------|-----------|-------------|-------------|
| Gradient Boosting   | 0.8653    | \$2,459.72  | \$4,451.78  |
| Random Forest       | 0.8522    | \$2,580.12  | \$4,660.84  |
| Ridge Regression    | 0.7836    | \$4,181.35  | \$5,648.51  |
| Linear Regression   | 0.7833    | \$4,181.19  | \$5,652.61  |

---

## How to Run This Project
1.  **Clone the repository**:
    ```bash
    git clone [https://your-repo-url.com/medical-cost-prediction.git](https://your-repo-url.com/medical-cost-prediction.git)
    ```
2.  **Create a virtual environment** (recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```
3.  **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the Jupyter Notebook**:
    Launch Jupyter and open the `medical_cost_prediction.ipynb` file to see the complete analysis.
    ```bash
    jupyter notebook
    ```
