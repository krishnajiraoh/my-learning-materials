# What is Machine learning?:

	• Is a set of techniques to make computers better at doing things than humans are traditionally better at


# Linear Regression:

	• Predicted value is continuous

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/linear_equation.png" height=300/> 
</p>

## Gradient Descent, Cost Function :

	• Is the algorithm / approach that finds the best fit line for a given training data set
	• i.e., minimize the cost function
	• Global minima

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/gradient_descent.png" height=300/> 
</p>

## Ex: of cost function: Mean Squared Error : MSE

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/mse.png" height=300/> 
</p>

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/mse_with_gradient.png" height=300/> 
</p>

# Logistic Regression :

	• Predicted value is categorical
	• Math : Sigmoid function
	• Converts input values into the range 0 to 1

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/logistic_reg.png" height=300/> 
</p>
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/logistic_reg_ex.png" height=300/> 
</p>

# Decision Tree :

## Entropy :
	• helps us to build an appropriate decision tree for selecting the best splitter. 
	• Entropy can be defined as a measure of the purity of the sub split. 
	• Entropy always lies between 0 to 1
	• Low entropy signifies HIGH INFORMATION gain and vice-versa

### information gain, gini impurity -> to read


# Support Vector Machine:

	• Maximize the margin i.e., the distance of the nearest datapoints from the decision boundary, among the classification groups

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/svm.png" height=300/> 
</p>

## Gamma 

	• High gamma -> datapoints are very close are considered 
	• Low gamma -> datapoints that relatively further are also considered for SV

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/gamma.png" height=300/> 
</p>

## Regularization (C): 

	• Same as above 
	• Overfitting vs underfitting

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/regualization.png" height=300/> 
</p>

## Kernel:
	• Generate new feature as a computation of the existing
	• Use the kernel to draw better boundaries
	• Ex: rbf, linear, etc

# Random Forest:

	• Sample the dataset, build decision tree for each of the sample, go with the majority vote for prediction
	• Model ensemble technique

# Cross Validation :
	• Evaluate model performance across models

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/cross_val.png" height=300/> 
</p>

# KFold:

## Stratified KFlod:
	• Splits the classes uniformly 

# Navie Bayes:

	• Assumption:
		○ Each feature makes an independent and equal contribution to the output
		○ Basically, we are trying to find probability of event A, given the event B is true. Event B is also termed as evidence.
		○ Conditional probability
		○ The different naive Bayes classifiers differ mainly by the assumptions they make regarding the distribution of P(xi | y).
		○ Ex: In Gaussian Naive Bayes, continuous values associated with each feature are assumed to be distributed according to a Gaussian distribution.
<iamges>
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/naive_bayes.png" height=300/> 
</p>
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/nb_ex.png" height=300/> 
</p>

## Types:
<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/nb_types.png" height=300/> 
</p>



# Hyper Parameter Tuning :

	• Optimizing the hyper params
	• Train_test_split is unreliable because of randomness in sampling
	• GridSearchCV:
		○ Execute all param combinations in Cross_ val_score 
		○ Hyperparam tuning for ONE estimator 

# L1 & L2 for reducing model overfitting 

## L1 Regularization :
	• Penalize higher values of coefficients / hyper params
	• L1 -> use Absolute value

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/l1.png" height=300/> 
</p>

## L2 Regularization :

	• Penalize higher values of coefficients / hyper params
	• L2 -> 2 stands for Square

<p align="center"> 
    <img src="https://github.com/krishnajiraoh/MyLearningMaterials/blob/main/Machine%20Learning/.images/l2.png" height=300/> 
</p>

# Metrics:

## Classification:

	• Accuracy
	• F1 score
	• Precision
	• recall

## Regression:

	• R2
	• RMSE
	• MSE
	• MAE
	• MAPE


