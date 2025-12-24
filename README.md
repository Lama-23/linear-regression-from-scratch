# linear-regression-from-scratch
This project implements Linear Regression, a fundamental Supervised Machine Learning algorithm used for predicting continuous values. The goal is to model the relationship between a dependent variable (y) and one or more independent variables (X).

## 1. The Mathematical Model
The model assumes a linear relationship:

<img width="506" height="118" alt="image" src="https://github.com/user-attachments/assets/3edf5314-9a82-44d3-b223-6777a4515358" />



Where:
- X: Feature matrix.
* θ(Theta): The parameter vector (Weights and Bias).
+ y: Target/Output vector.

  
## 2. Estimation Method (Loss Function)
To find the best-fitting line, we use the Mean Squared Error (MSE) as our Loss Function. It measures the average squared difference between the predicted values and the actual values.


## 3. Implementation Approaches
In this notebook, I explore the two primary ways to estimate the optimal parameters (θ):
- **A. The Analytical Approach: Normal Equation**


The Normal Equation is a mathematical formula that solves for θ directly in a single step without the need for iterations.
   **Formula:**

  <img width="500" height="90" alt="image" src="https://github.com/user-attachments/assets/d2417cc4-fadf-41a5-ac0b-214a96cb21d7" />


Pros: Exact solution, no hyperparameter tuning (no Learning Rate needed).


Cons: Computationally expensive for very large datasets (due to matrix inversion).



* **B. The Numerical Approach: Gradient Descent**
  
Gradient Descent is an optimization algorithm that minimizes the Loss Function by iteratively updating the weights in the opposite direction of the gradient.


 Process: Starts with random initialization and takes small steps (governed by the Learning Rate) towards the global minimum.
 
 Pros: Efficient for large-scale datasets and high-dimensional features.
 
 Cons: Requires Feature Scaling and careful tuning of the Learning Rat (α)


## 4. Key Assumptions & Constraints

For Linear Regression to perform optimally, several assumptions should hold true:


- Linearity: The relationship between the independent variables (X) and the dependent variable (y) must be linear.
* Independence: Observations in the dataset should be independent of each other.
+ Homoscedasticity: The variance of residual errors should be constant across all levels of the independent variables.
- No Multicollinearity: Independent variables should not be highly correlated with each other, as this can make the Normal Equation unstable.
* Sensitivity to Outliers: Since we use MSE (squaring the errors), the model is highly sensitive to outliers, which can disproportionately influence the slope of the regression line.

 

