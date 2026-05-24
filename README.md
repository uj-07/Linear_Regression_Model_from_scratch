# Linear_Regression_Model_from_scratch

A pure, from-scratch implementation of a Simple Linear Regression model using Python. This project avoids high-level machine learning libraries like Scikit-Learn for model training, opting instead to implement the mathematical **Closed-Form Solution (Ordinary Least Squares)** manually to predict salaries based on years of experience.

## Features

* **From-Scratch Math**: Custom-built `LR` class implementing Ordinary Least Squares (OLS) to calculate the optimal slope ($m$) and intercept ($b$).
* **Clear Evaluation**: Fully evaluated using standard statistical metrics ($R^2$ Score, MAE, RMSE).
* **Data Visualization**: Includes interactive visualizations showing the line of best fit and a dedicated residuals error plot.

---

## Mathematical Overview

The model fits a straight line to the training data using the classic linear equation:

$$y = m \cdot x + b$$

Instead of iterative gradient descent, this implementation uses the **Closed-Form Solution** to find the exact global minimum in one step:

### Slope ($m$) Formula:
$$m = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^{n} (x_i - \bar{x})^2}$$

### Intercept ($b$) Formula:
$$b = \bar{y} - m \cdot \bar{x}$$

*(Where $\bar{x}$ and $\bar{y}$ represent the mean values of the features and target, respectively).*

---

## Dataset & Performance

The model is trained on `Salary_Data.csv` (containing 30 records matching **Years of Experience** against **Salary**). 

After splitting the data (80% Train / 20% Test), the model extracted the following parameters:
* **Slope ($m$):** 9569.59
* **Intercept ($b$):** 24393.17

### Final Test Results:
| Metric | Value |
| :--- | :--- |
| **$R^2$ Score (Variance Explained)** | 0.8887 (88.87%) |
| **Mean Absolute Error (MAE)** | $6,802.78 |
| **Root Mean Squared Error (RMSE)** | $7,492.50 |

---

## Project Structure

```text
├── Linear_Regression_Model_from_scratch/
│   ├── Untitled.ipynb      # Jupyter notebook with the LR class, training, and plots
│   └── Salary_Data.csv     # The experience vs. salary dataset
│   └── README.md           # Project documentation
