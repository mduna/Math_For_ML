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

Linear regression uses methods like Ordinary Least Squares (OLS) to minimize the cost function:

$J(\beta) = \frac{1}{2m} \sum_{i=1}^{m} \left( \hat{y}_i - y_i \right)^2$

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

### 1.3.3. Train the Model
Fit the model on the training data to learn th coefficients.

### 1.3.4. Evaluate the Model
Evaluate using matrics like:
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R-squared ($R^{2}$)

### 1.3.5. Example Code
#### 1.3.5.1 Code and dataset
See the Code in the file scikit-learn.py. Test with a dataset called scikit-learn.csv. The dataset contains three columns:  
1. feature1: Size of the house in square feet
2. feature2: Number of bedrooms
3. target: Price of the house in $1000

#### 1.3.5.2. Expected Output
- The model will predict house prices based on size and the number of bedrooms
- You will see metrics Mean Squared Error (MSE) and R-squared ($R^{2}$)

#### 1.3.5.3 Explain Result
##### 1.3.5.3.1. Mean Squared Error (MSE)
MSE measures the average squared difference between the predicted values ($\hat{y}$) and the actual values (y)  

$MSE = \frac{1}{n} \sum_{i=1}^{n} \left( \hat{y}_i - y_i \right)^2$

**Where:**

* **n** The Number of data points.
* **ŷ<sub>i</sub>** The predicted value for the i-th sample.
* **y<sub>i</sub>** The actual value for the i-th sample.

##### 1.3.5.3.2. What It Means
- **Smaller MSE** indicates that the predictions are close to the actual values, which means the model is performing better.
- MSE penalizes large errors more than small onces because it squares the differences.

##### 1.3.5.3.3. Interpretation
- Units: MSE is in the squre of the target variable's unit. For example, if the target is the house prices in dollars, MSE will be in $(dollars)^{2}$
- A perfect model would have MSE = 0, meaning to no difference between predications and actual values.

##### 1.3.5.3.2. R-squared ($R^{2}$)
R-squared R² (Coefficient of Determination) explains how much of the variability in the target variable (y) is explained by the features (X) in the model.

**Formula**

$R^{2} = 1 - \frac{\text{Sum of Squared Residuals (SSR)}}{\text{Total Sum of Squares (TSS)}}$


**Where:** 

$SSR = \sum_{i=1}^{n} \left( y_i - \hat{y}_i  \right)^{2}$  Residuals (unexplained variance by the model).

$TSS = \sum_{i=1}^n (y_i - \bar{y})^{2}$  Total variance in the data

**What It Means:**  

* $R^{2}$ ranges from 0 to 1.
* $R^{2}$ = 1 : Perfect model; all variability in y is explained by X
* $R^{2}$ = 0 : The model explains none of the variability in y (no better than predicting the mean $\hat{y}$ )
* Negative $R^{2}$ : The model performs worse than a simple mean-based prediction  

**Interpretation**
* A higher $R^{2}$ value indicates a better fit of the model to the data.
* For example, $R^{2}$ = 0.85 implies 85% of the variability in y is explained by the features.

**Note:**

* R-squared can be misleading in some cases, such as when dealing with small datasets or when the model is overly complex.
* It's important to consider other metrics, such as adjusted R-squared and cross-validation, to evaluate model performance.

**For our scikit-learn.py code here, Interpreting MSE and R²**  

**Suppose:**   
MSE = 2500 (e.g., squared dollars)  
R² = 0.92  
**This means:**  
- MSE: On average, the squared error in predicted house prices is 2500. The smaller the value, the better the model predicts house prices.
- R²: 92% of the variability in house prices is explained by the model, suggesting it is highly effective.





