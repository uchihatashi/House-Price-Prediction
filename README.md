# House Price Prediction

## Problem Statement
A US-based housing company named **Surprise Housing** has decided to enter the Australian market. The company uses data analytics to purchase houses at a **price below their actual values and flip them on at a higher price**. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.
The company is looking at prospective properties to buy to enter the market. You are required to **build a regression model using regularisation** in order to predict the actual value of the prospective properties and decide whether to invest in them or not.

**The company wants to know:**

- Which variables are significant in predicting the price of a house, and
- How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.


### Business Goal 
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.


### Structure:

	-- data
	 	-- data_description.txt
	 	-- train.csv
	 -- House-Price-Prediction.ipynb
	 -- Problem Statement - Part II.pdf



### Building a model using Linear, Ridge and Lasso Regression
- Model A: Without log and scale on SalePrice.
- Model B: log on SalePrice and without StandardScaler()
- Model C: log on SalePrice with StandardScaler()

# Result:

## Model A: Ridge VS Lasso Without log and scale on SalePrice.
### For Ridge:
**Alpha: 40**

**R-squared value for Ridge**
- Train:  0.872
- Test:  0.863

**mean_squared_error value**
- Train:  28281.329
- Test:  29422.777

### For Lasso:
**Alpha: 100**

**R-squared value**
- Train:  0.899
- Test:  0.867

**mean_squared_error value**
- Train:  25187.870
- Test:  29057.064

*************

## Model B: Ridge VS Lasso after applying LOG
### For Ridge: 
**Alpha: 20**

**R-squared value for Ridge**
- Train:  0.910
- Test:  0.894

**mean_squared_error value**
- Train:  0.120
- Test:  0.129

### For Lasso:
**Alpha: 0.0001**

**R-squared value**
- Train:  0.948
- Test:  0.844

**mean_squared_error value**
- Train:  0.0913
- Test:   0.157

*************

## Model C: Ridge VS Lasso after applying Log()
### For Ridge: 
**Alpha: 20**

**R-squared value for Ridge**
- Train:  0.911
- Test:  0.894

**mean_squared_error value**
- Train:  0.299
- Test:  0.322

### For Lasso:
**Alpha: 0.0003**

**R-squared value**
- Train:  0.945
- Test:   0.857

**mean_squared_error value**
- Train:  0.235
- Test:   0.375

Here we can clearly see that **Ridge** did better cause **Lasso** seem like overfeeding and **train and test** have around **9%** gape. However **Ridge** have only **2%** gape.

************** ****

### Model C preformed the best and we will go with model C.

******************
******************
*****************
<br>
<br>


## Problem Statement - Part II

### Question 1
What is the optimal value of alpha for ridge and lasso regression? What will be the changes in the model if you choose double the value of alpha for both ridge and lasso? What will be the most important predictor variables after the change is implemented?


### Question 2
You have determined the optimal value of lambda for ridge and lasso regression during the assignment. Now, which one will you choose to apply and why?

### Question 3
After building the model, you realised that the five most important predictor variables in the lasso model are not available in the incoming data. You will now have to create another model excluding the five most important predictor variables. Which are the five most important predictor variables now?

### Question 4
How can you make sure that a model is robust and generalisable? What are the implications of the same for the accuracy of the model and why?
