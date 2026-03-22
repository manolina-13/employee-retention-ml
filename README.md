# Employee Retention Analysis using Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A machine learning project that analyzes employee retention using HR analytics data. This project performs exploratory data analysis (EDA) to identify key factors influencing employee attrition and builds a Logistic Regression model to predict whether an employee is likely to leave the organization.

---

##  Problem Statement

The objective of this project is to understand and predict employee attrition using HR analytics data. The study focuses on identifying critical factors—such as satisfaction level, salary, department, and workload—that contribute to employee turnover.

By performing exploratory data analysis (EDA) and building a Logistic Regression model, the project aims to provide insights into workforce behavior and develop a predictive system to estimate the likelihood of an employee leaving the organization.

---

##  Features

-   **Exploratory Data Analysis (EDA)**: Identifies patterns and relationships between employee features and retention.
-   **Data Visualization**: Uses Seaborn and Matplotlib to visualize the impact of salary and department on employee attrition.
-   **Feature Engineering**: Handles categorical variables using one-hot encoding.
-   **Machine Learning Model**: Implements Logistic Regression for employee attrition prediction.
-   **Model Evaluation**: Evaluates performance using confusion matrix, classification report, and accuracy (~79.5%).
-   **Insight Generation**: Highlights key factors such as satisfaction level, salary, and workload affecting employee turnover.

---

##  Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook / JupyterLab

---

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/employee-retention-ml.git
cd employee-retention-ml


# Create virtual environment
python -m venv venv

# Activate it (Windows)
venv\Scripts\activate

# Activate it (macOS/Linux)
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

---

##  Running the Project

```bash
jupyter notebook

