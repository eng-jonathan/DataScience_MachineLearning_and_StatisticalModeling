## Queens College - Math 390.4/342W: Data Science via Machine Learning and Statistical Modeling 
Shortcuts: 
[Labs](https://github.com/eng-jonathan/QC_MATH_342/tree/master/labs) |
[Syllabus](https://github.com/eng-jonathan/QC_MATH_342/blob/master/syllabus/syllabus_math342.pdf) |
[Modeling Essay](https://github.com/eng-jonathan/QC_MATH_342/tree/master/modeling_essay) | 
[Final Project](https://github.com/eng-jonathan/QC_MATH_342/tree/master/final_project)
 
___
 
Course Overview:
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

Incorporated Topics
* Basic Probability Theory: axioms, conditional probability, in/dependence
* Modeling with discrete random variables: Bernoulli, Hypergeometric, Binomial, Poisson, Geometric, Negative Binomial, Uniform Discrete and others
* Expectation and variance
* Modeling with continuous random variables: Exponential, Uniform and Normal
* Frequentist confidence intervals and hypothesis testing for one-sample proportions
* Basic visualization of data: plots, histograms, bar charts
* Linear algebra: Vectors, matrices, rank, transpose
* Programming: basic data types, vectors, arrays, control flow (for, while, if, else), functions
___
[Modeling Essay](https://github.com/eng-jonathan/QC_MATH_342/tree/master/modeling_essay)
* [Assignment](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/modeling_essay/modeling_essay%20_prompt.pdf) | [Essay](https://github.com/eng-jonathan/QC_MATH_342/blob/master/modeling_essay/modeling_essay.pdf)
* "What Makes a Marriage Successful is not Understood, and Will Never Be Understood." It incorporates the  creation of a mathematical model, including feature selection, data training methods, and possible output errors. 
* Prompt: It is your job to interpret the above prompts and redefine them in your own words, i.e. you must limit, scope and concretize the above which are deliberately open-ended and nebulous. To argue your point, you will need to formulate a mathematical model with phenomenon(s) that can be measured (explain how) and characteristics of the units under consideration. You will need to clearly defne what "models" are, how your model is mathematical and discuss their limitations. In context of your prompt, you must appropriately explain the concepts we learned / will learn in class, including but not limited to t,f,g,h∗,δ,e,t,z1,...,zt,D,H,A,n,p, x·1,...,x·p, x1·,...,xn·,X,y,Y, supervised learning, the fidelity of the measurement process, extrapolation, interpolation, stationarity, overfitting, validation (in-sample vs. out-of-sample), model selection, machine learning, etc. 
___
[Final Project](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/tree/master/final_project):
* [Assignment](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject_prompt.pdf) | [Report](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject.pdf) | [R Code](https://github.com/eng-jonathan/QC_MATH_342_DataScience_via_MachineLearning_and_StatisticalModeling/blob/master/final_project/math3904_finalproject.Rmd)
* Uses Supervised Machine Learning to beat Zillow.com’s “zestimates.” It’s written in RStudio using R and incorporates data manipulation techniques such as data removal, munging and imputation, and linear and forest regressions
* Prompt: You will be writing a report about a prediction model for apartment selling prices in Queens, NY using the dataset found on github, housing_data_2016_2017.csv where the outcome to be predicted is the column named sale_price. This dataset is the raw data representation found at MLSI. The limitation on the data population for what you will be asked to predict will be “Queens, NY” as location and home types “Condo / homeowner assoc.” and “Co-op” up to a maximum sale price of $1M sold between February, 2016 and February, 2017 and limited to the zip codes found in Table . The dataset was harvested with Amazon’s MTurk and it is a raw download from their system.
