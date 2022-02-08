1. What is bias-variance tradeoff?
link: https://www.youtube.com/watch?v=YIPsfEtJppE

Consider that we have a data set. We create N random subsets of the data. We train a model for each subset, so we have N models. 

If all the models give similar results (for example, we are performing binary classification and most of the models give the same class as the output) then we can say that the models are biased. Biased models are overly simple. They perform the classification on the basis of a very small subset of features. For example, suppose you have 10 features to predict if someone will get admitted to a college and a biased model will simply classify on the basis of gender. Biased models are robust to minor variations in the data.


Now suppose the models we build takes into consideration all the 10 features and they follow the patterns in the data very closely. These models are overly complex and will try to learn patterns which are not actually there (noise), hence they will fail to generalise in the test set. These models are said to have high variance. No two models will give similar or consistent results as they are influenced by noises of the data. Small change in the training data will create major impact on the outcome. 


Now increasing bias will decrease variance and increasing variance will decrease bias (hence the Tradeoff). Ideal models will have reasonably low bias and reasonably low variance. 

2. What is multi-collinearity?

When the independent variables in a regression model are correlated, it is called multi-collinearity. It can be of 2 types:
structural - if we have X as a feature and we include X^2 as a feature too
data - observational diffiulties, where we fail to identify if 2 features are correlated

2. Why is Multicollinearity a problem?
Multi-collinearity may not affect the accuracy of the model as much. But we might lose reliability in determining the effects of individual features in the model - and that becomes a problem when it comes to interpretability. 

The coefficient estimates can swing wildly based on which other independent variables are in the model. The coefficients become very sensitive to small changes in the model.

Multicollinearity reduces the precision of the estimated coefficients, which weakens the statistical power of your regression model. You might not be able to trust the p-values to identify independent variables that are statistically significant.

3. How to detect Multicollinearity?
There are some ways to detect multicollinearity:
Multicollinearity can be detected using VIF (Variable Inflation Factors).  VIF determines the strength of the correlation between the independent variables. It is predicted by taking a variable and regressing it against every other variable.





