# Neural Network Charity Analysis


## Overview of the analysis: 
Help  Alphabet Soup to create a binary classifier that is capable to predict if applicants will be successful if the company founded their ideas.
## Results: 
### o	Data Preprocessing

### What variable(s) are considered the target(s) for your model?
The data considered the target for this model was “IS_SUCCESSFUL” column.

### What variable(s) are considered to be the features for your model?
 
For the first try of the model the following features were taken into consideration:

-	**APPLICATION_TYPE** Alphabet Soup application type.
-	**AFFILIATION** Affiliated sector of industry.
-	**CLASSIFICATION** Government organization classification.
-	**USE_CASE** Use case for funding.
-	**ORGANIZATION** Organization type.
-	**STATUS** Active status.
-	**INCOME_AMT** Income classification.
-	**SPECIAL_CONSIDERATIONS** Special consideration for application.
-	**ASK_AMT** Funding amount requested.

For the optimization the “SPECIAL_CONSIDERATIONS” was dropped and “ASK_AMT” was divided into bins.

### What variable(s) are neither targets nor features, and should be removed from the input data?

For the first try of the model:
**EIN** and **NAME** Identification columns

For the optimization:
**EIN** and **NAME** Identification columns
**SPECIAL_CONSIDERATIONS** Special consideration for application


### o	Compiling, Training, and Evaluating the Model
### How many neurons, layers, and activation functions did you select for your neural network model?

For the first try:

The input features were “len(X_train[0])” which was 43 neurons. Two hidden layers were selected with 80 and 30 neurons each. Both hidden layer activation functions were “relu” and the output activation function was “sigmoid”. 

![](https://github.com/KatiuscaQ/Neural_Network_Charity_Analysis/blob/main/Resources/first_model.PNG)

For the optimized model:

Many models were executed during this study, the following is describing the features of the model with the highest accuracy:
The input was 43 neurons, there were three hidden layers: 80, 30, and 10 neurons respectively, and all hidden layers and output layer were run with the “Sigmoid” activation function.

![](https://github.com/KatiuscaQ/Neural_Network_Charity_Analysis/blob/main/Resources/best_model.PNG)

### o	Were you able to achieve the target model performance?
No. The target model performance was 75% or up. The highest any of the models executed in this study was 73%. 

### o What steps did you take to try and increase model performance?

Different steps and models were performed:
-	In addition to EIN and NAME columns, the column SPECIAL_CONSIDERATIONS was also removed.
-	The columns APPLICATION_TYPE, CLASSIFICATION, and ASK_AMT were divided into bins.
-	*Random Forest Classifier* was used to experiment with the dataset and the accuracy for this model was 72.8%.
-	SVM model was implemented but with not high expectations. The accuracy of this model was 71.7%
-	Different deep neural networks were tried. Layers where added and removed as well as the activation functions were interchanged between layers.

## Summary: 

After all the models tried on this study, my recommendation will be to:

-	Add more data to the dataset. 
-	Experiment with the Leaky ReLU and Tanh functions.
-	Improve the models of this study.

The reason of these recommendations are made since these recommendations were not performed in this study.
