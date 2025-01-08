# Math_For_ML
Math for Machine Learning

## 1. Linear Regression
### 1.1. What is Linear Regression
Linear regression attempts to model the relationship between:

Independent variables (features) (𝑋) and
Dependent variable (target) (y)

The model assumes a linear relationship:
**Linear Regression Equation**
The general form of a linear regression equation is:

$y = \beta_0 + \beta_1x_1 + \beta_2x_2 + ... + \beta_nx_n + \epsilon$

**Where:**

* **y:** Target variable (the value we are trying to predict)
* **x1, x2, ..., xn:** Input features (independent variables)
* **β0, β1, ..., βn:** Coefficients (weights) that determine the influence of each input feature on the target variable. 
    * **β0:** Intercept (the value of y when all input features are zero)
* **ϵ:** Error term (represents the difference between the predicted value of y and the actual value)

This equation represents a linear relationship between the target variable and the input features. The goal of linear regression is to find the values of the coefficients (β0, β1, ..., βn) that best fit the data and minimize the error term.

### 1.2. Type of Linear Regression
#### 1.2.1. Simple Linear Regression
One feature:  
$y = \beta_0 + \beta_1x_1 + \epsilon$

#### 1.2.2. Multiple Linear Regression
Multiple features:  
$y = \beta_0 + \sum_{i=1}^{n} \beta_i x_i + \epsilon$

### 1.3. Steps to Implement Linear Regression
#### 1.3.1. Prepare the Data
1. Collect and clean the dataset
2. Separate the dataset in features (X) and target (y)
3. Split into training and testing sets

#### 1.3.2. Build the Model

## Linear Regression: Cost Function

Linear regression aims to find the best-fitting line (or hyperplane in higher dimensions) that minimizes the difference between the predicted values and the actual values of the target variable. 

**Cost Function**

A common cost function used in linear regression is the **Mean Squared Error (MSE)**, also known as the **Ordinary Least Squares (OLS)** cost function. It is defined as:

<span class="math-inline">J\(\\beta\) \= \\frac\{1\}\{2m\} \\sum\_\{i\=1\}^\{m\} \\left\( \\hat\{y\}\_i \- y\_i \\right\)^2</span>

**Where:**

* **J(β):** The cost function, which measures the average squared difference between the predicted values and the actual values.
* **m:** The number of samples in the training dataset.
* **ŷ<sub>i</sub>:** The predicted value for the i-th sample.
* **y<sub>i</sub>:** The actual value for the i-th sample.

**Minimizing the Cost Function**

The goal of linear regression is to find the values of the model's parameters (β) that minimize the cost function. This is typically achieved using optimization algorithms such as gradient descent.

**Key Points:**

* The OLS cost function penalizes large errors more severely than small errors due to the squaring of the differences.
* Minimizing the MSE leads to the line that best fits the data in a least-squares sense.

This Markdown code effectively presents the cost function used in linear regression, including:

* **Clear and concise explanation:** It explains the purpose of the cost function and its role in linear regression.
* **Mathematical representation:** The equation is correctly formatted using LaTeX syntax within the Markdown.
* **Definitions of terms:** All variables in the equation are clearly defined.
* **Key points:** It highlights the significance of the OLS cost function and its implications for model fitting.