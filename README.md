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

```

##  Running the Project

```bash
jupyter notebook
```
Open:
```bash
notebooks/employee_retention_analysis.ipynb
```
Run all cells to reproduce the analysis.


## Key Insights

- Employees with **low satisfaction levels** are more likely to leave.
- **Low salary** is strongly associated with higher attrition.
- Certain **departments show higher turnover trends**.
- Workload and time spent in the company also influence retention.

## Model Performance

- **Model Used**: Logistic Regression  
- **Accuracy**: ~79.5%  

The model performs well in predicting employees who stay but has relatively lower recall for employees who leave, indicating scope for improvement.

## Conclusion

In this project, we analyzed employee retention using HR analytics data and identified key factors influencing employee attrition. Exploratory Data Analysis (EDA) revealed that variables such as satisfaction level, salary, and workload have a significant impact on whether employees leave the organization.

A Logistic Regression model was developed to predict employee attrition, achieving an accuracy of approximately 79.5%. While the model performs reasonably well in predicting employees who stay, it shows relatively lower performance in identifying employees who leave, indicating scope for improvement.

Overall, this study demonstrates how data-driven approaches can help organizations understand employee behavior and take proactive measures to improve retention.


## Future Improvements

- Use advanced models like Random Forest or XGBoost
- Handle class imbalance for better prediction
- Perform hyperparameter tuning
- Add ROC curve and precision-recall analysis

## License

This project is distributed under the MIT License. See `LICENSE` for more information.

## Contact

Manolina Das - [GitHub Profile](https://github.com/manolina-13)

Project Link: [https://github.com/manolina-13/AI-powered--Study-Buddy](https://github.com/manolina-13/AI-powered--Study-Buddy)

