# Customer-Segmentation-complete EDA and Machine-Learning-model-in-Spark-framework-using-PySpark
Customer segmentation model developed using Spark ML
Models used are,
**Logistic Regression** – This is a very popular statistical classification technique that uses a logit function to model the binary target variable. 
 

Here, to identify the best parameters of the logistic regression model, I have used hyper parameter tuning. Using ParamGridBuilder() different set of parameter values are assigned to parameters such as ‘regParam’, ‘maxIter’, ‘tol’, and ‘elasticNetParam’. The best combination of parameters is chosen and the best model is returned by TrainValidationSplit() function in PySpark. Cross validation is done with a training ration of 0.8. 
MulticlassClassificationEvaluator() is used to evaluate the model. The evaluation results are, 

From the evaluation metrics, we can see that the model has returned a good accuracy score of 88.86% with precision 87.97%. The ROC score is also good for this

**Random Forest Classifier-** This classifier created different decision trees from the subsets of data and the do a voting aggregation to identify the best model. These are robust to outliers. 
 
Hyper parameter optimization id done to identify the best model. Different set of parameters ‘maxDepth’, ‘maxBins’, ‘numTrees’, ‘impurity’, ‘minInstancesPerNode’ for parameter tuning. TrainValidationSplit() method returned the best model after doing the cross validation
The evaluation results of the model are,
 
Random Forest modelling has resulted in an accuracy of 90.68% with Precision score 90.14%. ROC score is also quite good with 93.80%

**Support Vector Classifier-** this is another popular classifier which uses a hyperplane to separate the data points of different classes. 
 
Hyper parameter optimization is done on the Linear SVC to optimize the model with best parameters. Parameters such as ‘regParam’, ‘tol’, and ‘maxIter’ were given a set of values for tuning. Using TrainValidationSplit(), the model is built with best parameters by doing a cross validation with a training ratio of 80%. 

Model evaluation is performed using Multiclass Evaluator() and the results are as follows,
 
Support vector machine classifier has given an accuracy of 89% with a precision of 88%. The ROC score is 90%.

