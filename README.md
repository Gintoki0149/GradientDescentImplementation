# GradientDescentImplementation
- This project is an implementation of basic machine learning algorithms.
- The problem statement included a diabetes dataset.
- The dataset included the following columns:
    - Pregnancies
    - Glucose
    - BloodPressure
    - SkinThickness
    - Insulin
    - BMI
    - DiabetesPedigreeFunction
    - Age
    - Outcome(Whether the patient has diabetes or not)
**keywords:** Gradient Descent, Polynomial Regression, Classification<br>
**Libraries Used:** 
- numpy was used for faster computation and matrix operations
- sklearn was used for splitting data into training and testing sets
- matplotlib was used for data visualization

## Gradient Descent
**Use:** This algorithm very cleverly uses the defenition of the gradient to update weights of a particular regression problem correctly.
The gradient is defined as the direction of steepest increase. The algorithm takes advantage of this and goes in the direction opposite to that given by the gradient.
Thus the weights move closer to a minima.<br>
**The Sum of Squared Errors was used**<br><br>
&emsp;&emsp;**Batch-Gradient:** 
- The weights are updated after each epoch
- Computation was done in the form of matrices
- The gradient is calculated as J(w) = X<sup>T</sup>Xw - X<sup>T</sup>y where X is the input matrix, w is the weight vector and y is the output vector 
- After calculating J(w), w = w - a*J(w) where a is the learning rate<br><br>
  **Stochastic-Gradient:** <br>
* The weights are updated for each sample in the dataset in all the epochs
* weights are modified using the equation w<sub>i</sub> = w<sub>i</sub> - a*(y'-y)*x<sub>i</sub> where y' represents the predicted value for the i<sup>th</sup> data sample

## Polynomial Regression
**Use:** This algorithm is used in case of a polynomial relation between the input variable and the output variable. It uses the same intuition as normal linear regression however the features are powers of the sample variable<br>
**Regularization:** If we talk about polynomial regression, as the degree of the polynomial increases the flexibility of the hypotheses function increases and the model starts learning the randomness of the data points. This leads to over-fitting which leads to poor performance on unseen data. To overcome this, an additional penalty term is added to the usual error function to keep overfitting in check
<br>
- **L1 regularization:** The penalty term added is proportional to the sum of the magnitudes of the magnitudes of the weights. The constant of proportionality is called as the regularization rate denoted by the greek alphabet lambda<br>
In such a case the new error function becomes E(w) + (regularization rate)*||w||<sub>1</sub><br>
It is also called Lasso Regularization
- **L2 regularization:** The penalty term is proportional to the sum of the squares of magnitudes of the weights
  In such a case the new error function becomes E(w) + (regularization rate)*||w||<sub>2</sub><br>
  It is also called Ridge Regularization


 
