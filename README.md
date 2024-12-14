# Polynomial Regression with Gradient Descent

#### This project was developed as a part of Intelligent Systems: Machine Learning subject, for the Masters in Information and Computer Science (AI specialization) at the University of Luxembourg.

This project implements **Polynomial Regression** optimized using **Gradient Descent**, built entirely from scratch without using libraries like Scikit-Learn. It demonstrates how to manually compute the cost function, gradients, and parameter updates while processing data from a dataset in Excel format.

## Features
- Implements a **quadratic polynomial regression model**:
  \[
  h_{\theta}(x) = \theta_2 x^2 + \theta_1 x + \theta_0
  \]
- Uses a **custom cost function**:
  \[
  J(\theta) = \frac{1}{4n} \sum_{i=1}^{n} \left( y^{(i)} - h_{\theta}(x^{(i)}) \right)^4
  \]
- **Gradient Descent Optimization**:
  - Updates model parameters (\( \theta_2, \theta_1, \theta_0 \)) iteratively using partial derivatives of the cost function.

## Workflow
1. **Data Input**:
   - Reads data from an Excel file with two columns:
     - **Column 1**: Input feature (Temperature in Celsius, \(X\))
     - **Column 2**: Output target (Net hourly electrical energy output, \(Y\)).
   - Each row represents one data point.

2. **Data Preprocessing**:
   - Normalizes input features for stable gradient descent.

3. **Model Training**:
   - Implements the gradient descent algorithm to minimize the cost function and find optimal model parameters.

4. **Model Evaluation**:
   - Outputs the final model parameters (\( \theta_2, \theta_1, \theta_0 \)).
   - Tracks the cost during training for monitoring convergence.

## How to Use
1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Prepare an Excel file with your dataset (two columns: \(X\) and \(Y\)).

3. Install dependencies for reading Excel files:
   ```bash
   pip install numpy pandas openpyxl
   ```

4. Run the Python script:
   ```bash
   python polynomial_regression.py
   ```

5. Observe the model's progress (cost values, gradients) and final predictions.

## Key Files
- **polynomial_regression.py**: Main script for loading data, training the model, and optimizing parameters.
- **data.xlsx**: Example dataset (replace with your own data).

## Dependencies
- Python 3.7+
- Libraries:
  - `numpy`: For matrix operations and numerical calculations.
  - `pandas`: For reading Excel files and preprocessing data.
  - `openpyxl`: Required for reading `.xlsx` files.

## Example Dataset
| X (Temperature in °C) | Y (Energy Output in MW) |
|------------------------|-------------------------|
| 15.2                   | 440.5                  |
| 20.3                   | 452.7                  |
| 25.7                   | 465.2                  |

## Output
- **Model Parameters**: Final values of \( \theta_2, \theta_1, \theta_0 \).
- **Training Cost**: Final cost of the model after convergence.
- **Prediction**: Example predictions for given input data.

## Limitations
- Only supports quadratic models (degree-2 polynomial regression).
- Gradient descent can be sensitive to the choice of the learning rate (\( \alpha \)).

## Acknowledgments
This project is built from scratch based on machine learning principles, inspired by concepts from:
- *Andrew Ng’s Machine Learning Course*
- *Pattern Recognition and Machine Learning* by Christopher M. Bishop

