# Data Science via Machine Learning and Statistical Modeling 
[Labs](https://github.com/eng-jonathan/QC_MATH_342/tree/master/labs) |
[Syllabus](https://github.com/eng-jonathan/QC_MATH_342/blob/master/syllabus/syllabus_math342.pdf) |
[Marriage Model](https://github.com/eng-jonathan/QC_MATH_342/tree/master/modeling_essay) | 
[Queens Apartment Price Predictions](https://github.com/eng-jonathan/QC_MATH_342/tree/master/final_project)
 
___
### [Mathematical Model on Marriage Success](https://github.com/eng-jonathan/QC_MATH_342/tree/master/modeling_essay)
* [Prompt](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/modeling_essay/modeling_essay%20_prompt.pdf) | [Essay](https://github.com/eng-jonathan/QC_MATH_342/blob/master/modeling_essay/modeling_essay.pdf)
* Creates a mathematical model to explain what makes a success marriage will never be understood. It incorporates feature selection, data training methods, and possible output errors. 
___
### [Can you beat Zillow at Predicting Apartment Prices in Queens?](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/tree/master/final_project)
* [Prompt](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject_prompt.pdf) | [Report](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject.pdf) | [R Code](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject.Rmd)
* Uses Supervised Machine Learning to beat *Zillow.com’s “zestimates”* due to its inaccuracy on Queens apartment predictions. It’s developed in *R* and incorporates data manipulation techniques such as data removal, munging, and imputation, and linear and forest regressions.
* Highlights
```
#Split Data into Test and Train Indices
prop_test = 0.2
test_indices = sample(1 : nrow(newdata), round(prop_test * nrow(newdata)))
test_indices = sample(1 : nrow(newdata), round(prop_test * nrow(newdata)))
newdata_test = newdata[test_indices, ]
y_test = newdata_test[ ,1]
X_test = newdata_test[ ,2:ncol(newdata_test)]
train_indices = setdiff(1 : nrow(newdata), test_indices)
newdata_train = newdata[train_indices, ]
y_train = newdata_train[ ,1]
X_train = newdata_train[ ,2:ncol(newdata_train)]
```

```{r, warning = FALSE}
#Bagging and Regression Trees (Random Forest)
num_trees = 500
optimal_mtry = tuneRF(X, y, mtryStart = 1, ntreeTry = num_trees, stepFactor =  2, plot = FALSE, doBest = FALSE)
mod_bag = YARF(X_test, y_test, num_trees = num_trees, calculate_oob_error = FALSE, mtry = optimal_mtry[nrow(optimal_mtry)]) 
mod_rf = YARF(X_test, y_test, num_trees = num_trees, calculate_oob_error = FALSE, mtry = optimal_mtry[nrow(optimal_mtry)])
YARF_update_with_oob_results(mod_bag)
YARF_update_with_oob_results(mod_rf)
rmse_bag = sd(y_test - predict(mod_bag, data.frame(X_test)))
rmse_rf = sd(y_test - predict(mod_rf, (X_test)))
cat("\nrmse_bag:", rmse_bag, "\nrmse_rf:", rmse_rf, "\n\ngain:", (rmse_bag - rmse_rf) / rmse_bag * 100, "%\n")
```

___ 
### Course Overview:
* Philosophy of modeling and learning using data
* Prediction via the ordinary linear model including orthogonal projections, sum of squares identity, R2 and RMSE
* Polynomial and interaction regressions
* Prediction with machine learning including neural nets (the perceptron), support vector machines and the tree methods CART, bagged trees and Random Forests
* Probability estimation using logistic regression, asymmetric cost classifiers and the ROC / DET performance curves
* Underfitting vs. overfitting and the bias-variance decomposition / tradeoff
* Model validation including out of sample techniques such as cross validation and bootstrap validation
* Correlation vs. causation, causal models, lurking variables and interpretations of linear model coefficients
* Extrapolation
* The R language will be taught formally from the ground and up as well as visualization using the ggplot library and manipulation using the dplyr and data.table libraries.

### Incorporated Topics
* Basic Probability Theory: axioms, conditional probability, in/dependence
* Modeling with discrete random variables: Bernoulli, Hypergeometric, Binomial, Poisson, Geometric, Negative Binomial, Uniform Discrete and others
* Expectation and variance
* Modeling with continuous random variables: Exponential, Uniform and Normal
* Frequentist confidence intervals and hypothesis testing for one-sample proportions
* Basic visualization of data: plots, histograms, bar charts
* Linear algebra: Vectors, matrices, rank, transpose
* Programming: basic data types, vectors, arrays, control flow (for, while, if, else), functions
___

