# CarrierPlanAnalysis

### Objective
To understand the importance of customer relationship, customer details and accoutn type with the Telecommunication company that is pitching them a new carrier plan.

### Problem Statement
1. To classify customers into accepting or rejecting a Carrier Plan based on customer attributes.
2. Comparirions of top 2 best performing Supervised Classification models (In this analysis, SVM and Logistic Regression)
3. To predict if an existing customer will choose a new plan being pitched to them or not.


### Table of Content
1. Importing Libraries
2. Data Cleaning
3. Missing Value Analysis
      <br> - Numerical Features
      <br> - Categorical Features
4. Outlier Analysis
5. EDA
6. Univariate & Bivariate Analysis
7. Feature Engineering
8. Logistic Regression Modelling
     <br> - Base Model creation
     <br> - Class Imbalance Handling
     <br> - Regularization (Ridge, Lasso, ElasticNet)
     <br> - GridSearch
9. SVM Modelling
     <br> - Base Model creation
     <br> - Class Imbalance Handling
     <br> - Kernel Selection
     <br> - GidSearch
10. Comparision of both models
11. Summary


### Conclusion

Technical Conclusion:
SVM is a much better classification than Logistic regression. 

- This is because when we do margin maximization, the distinction between class is more stronger. 
- They are better at handling non linearity in variables using kernels. 
- They are robust to outliers.
- The risk of overfitting is less in Support Vector Machine models compared to Logistic Regression.
- Assumption of Logistic is the linearity in variables which is not necessary for SVM, leading to better performance for SVM
- The final model we chose is the SVM model. The equation followed by the SVM has degree 4 polynomial function. This means that it is a non linear with a high complexity. Non linearity in the model tells us about how the features are associated with the Target. 
- Even with such a complex equation that the model would overfit had it not been for an SVM proves that the SVM is robust to outliers.
- The lambda parameter which is the inverse of C, is low. This tells us that we are not regularizing the error term.
- The optimal parameters given by GridSearch tells us that, we need to chose a polynomial equation of degree 4 with low regularization. The model need not be regularized.

Industrial Conclusion:
This model was created to predict if an existing customer will accept the new plan (1) or Not (0). There were numerical as well as categorical attributes for each customer that was used in the modelling.

- The prediction depends on personal information of the customer, location of the customer, occupation, designation & salary of the customer, feedback provided by customer as well as the account they have currently with the Telecommunication company and the new plan being pitched to them.
