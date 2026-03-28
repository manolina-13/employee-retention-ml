# Employee Retention Analysis using Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A machine learning project that analyzes employee retention using HR analytics data. This project performs exploratory data analysis (EDA) to identify key factors influencing employee attrition and builds a Logistic Regression model to predict whether an employee is likely to leave the organization.

---

##  Problem Statement

The objective of this project is to understand and predict employee attrition using HR analytics data. The study focuses on identifying critical factors—such as satisfaction level, salary, department, and workload—that contribute to employee turnover.

By performing exploratory data analysis (EDA) and building a Logistic Regression model, the project aims to provide insights into workforce behavior and develop a predictive system to estimate the likelihood of an employee leaving the organization.

---
## Technical Execution Flow

The project operates through a three-phase pipeline: Encoding, Simulated Transmission, and Decoding.

### 1. Encoding Phase (Sender Side)
When a user sends a message (e.g., "hi"), the following steps occur:
- **String to Binary:** The text is converted into a continuous 8-bit ASCII binary string. 
- **Redundancy Calculation:** The system calculates the number of parity bits ($r$) required for the data length ($k$) using the formula $2^r \ge k + r + 1$.
- **Bit Mapping:** A new bit array of length $n = k + r$ is created. Data bits are placed in all positions except those that are powers of two ($1, 2, 4, 8 \dots$).
- **Parity Computation:** Each parity bit at position $2^i$ is calculated by performing an XOR operation on a specific subset of data bits.

### 2. Transmission & Error Injection (Server Side)
To demonstrate the robustness of the Hamming code, the server acts as a "noisy channel":
- **Packet Interception:** The server receives the encoded bitstream.
- **Bit-Flipping:** The server intentionally selects one random index in the bitstream and inverts its value ($0 \to 1$ or $1 \to 0$).
- **Relay:** The corrupted packet is then forwarded to the intended recipient.

### 3. Decoding Phase (Receiver Side)
Upon receiving the corrupted bitstream, the client performs the following:
- **Syndrome Calculation:** The client re-calculates the parity bits. If the received parity bits do not match the calculated ones, a "Syndrome" is generated.
- **Error Localization:** The Syndrome value corresponds exactly to the 1-based index of the corrupted bit.
- **Bit Correction:** The client flips the bit at that specific index back to its original state.
- **Binary to String:** The parity bits are stripped away, and the corrected binary is converted back into ASCII text.

---

## Concrete Example: Transmitting the letter "B"

Here is a simplified walkthrough of a single-character transmission:

**1. Data Preparation:**
- Character: `B`
- ASCII Binary ($k=8$): `01000010`

**2. Encoding:**
- Required parity bits ($r$): 4 bits (Positions 1, 2, 4, 8)
- Total bits ($n$): 12 bits
- Encoded Bitstring: `P1 P2 D1 P4 D2 D3 D4 P8 D5 D6 D7 D8`
- Calculated result: `110110000010`

**3. Server-Side Corruption:**
- Server flips bit at **Index 7**.
- Received Bitstring: `110110100010` (Notice the 7th bit changed from `0` to `1`).

**4. Client-Side Correction:**
- Client calculates the Syndrome.
- Resulting Syndrome: `0111` (Binary for **7**).
- **Action:** Client flips the bit at Index 7 back to `0`.
- **Final Result:** `110110000010` -> Stripped to `01000010` -> ASCII `B`.

This process ensures that even though the server corrupted the data, the recipient sees the correct message `[B]` rather than an unreadable or incorrect character.

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



