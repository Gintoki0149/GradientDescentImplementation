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
**The Sum of Squared Errors was used**<br>
We performed linear regression to predict the outcome column values. Then we used a discriminant function to label all samples giving value of outcome greater than or equal to 0.5 to class 1 and others to class 0.
<br>
<br>
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
**Regularization:** If we talk about polynomial regression, as the degree of the polynomial increases the flexibility of the hypotheses function increases and the model starts learning the randomness of the data points. This leads to over-fitting which leads to poor performance on unseen data. To overcome this, an additional penalty term is added to the usual error function to keep overfitting in check. A procedure similar to gradient descent was carried out and the achieved accuracy was 75% with a quadratic polynomial.
<br>
- **L1 regularization:** The penalty term added is proportional to the sum of the magnitudes of the magnitudes of the weights. The constant of proportionality is called as the regularization rate denoted by the greek alphabet lambda<br>
In such a case the new error function becomes E(w) + (regularization rate)*||w||<sub>1</sub><br>
It is also called Lasso Regularization
- **L2 regularization:** The penalty term is proportional to the sum of the squares of magnitudes of the weights
  In such a case the new error function becomes E(w) + (regularization rate)*||w||<sub>2</sub><br>
  It is also called Ridge Regularization

## Logistic Regression
**Use:** This algorithm is used when we want to classify our samples into different classes. The Algorithm uses the sigmoid function to calculate the probability of a sample to belong to class 1. The probability of sample belonging to class 0 is accordingly calculated as 1 - sigmoid(x). Based on the prediction of the sigmoid we predict to which class the sample belongs to(sigmoid less than 0.5 implies class 0 else class 1). We achieved an accuracy of 84% using this algorithm.

## Least Squares Classification
**Use:** For this algorithm we use a one hot encoding to specify which a particular sample belonged to. Thus we get a $n*k$ matrix where n is the number of samples in the dataset and k is the number of classes we want. We achieved an accuracy of 82% using this algorithm.

 
