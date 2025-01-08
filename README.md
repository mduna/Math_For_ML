# Math_For_ML
Math for Machine Learning

## Linear Regression
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