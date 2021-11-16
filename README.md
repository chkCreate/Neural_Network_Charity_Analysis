# Neural_Network_Charity_Analysis
## Background
Using machine learning and neural networks, I used the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup\.

From Alphabet Soup’s business team, I received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years\. Within this dataset are a number of columns that capture metadata about each organization, such as the following\:

EIN and NAME—Identification columns\
APPLICATION_TYPE—Alphabet Soup application type\
AFFILIATION—Affiliated sector of industry\
CLASSIFICATION—Government organization classification\
USE_CASE—Use case for funding\
ORGANIZATION—Organization type\
STATUS—Active status\
INCOME_AMT—Income classification\
SPECIAL_CONSIDERATIONS—Special consideration for application\
ASK_AMT—Funding amount requested\
IS_SUCCESSFUL—Was the money used effectively

For this exercise, I will perform the following actions:
1. Preprocessing Data for a Neural Network Model
2. Compile, Train, and Evaluate the Model
3. Optimize the Model

## Results
### Data Preprocessing
1. What variable(s) are considered the target(s) for your model\?
  
IS_SUCCESSFUL variable is the binary classifier that demonstrates whether the applicants were successful with the funding by Alphabet Soup; and therefore, should be the target for this model\.

2. What variable(s) are considered to be the features for your model\?
  
The following variables should be considered as features for the model:
APPLICATION_TYPE—Alphabet Soup application type\
AFFILIATION—Affiliated sector of industry\
CLASSIFICATION—Government organization classification\
USE_CASE—Use case for funding\
ORGANIZATION—Organization type\
STATUS—Active status\
INCOME_AMT—Income classification\
SPECIAL_CONSIDERATIONS—Special consideration for application\
ASK_AMT—Funding amount requested

3. What variable(s) are neither targets nor features, and should be removed from the input data\?
  
EIN and NAME are identification columns, and have no impact to the model\. 

### Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why\?
   
The first hidden layer utilized the "relu" activation function, and had 80 neurons in the original model\. Then, the second hidden layer used the same "relu" activation function, which output 30 neurons\.

2. Were you able to achieve the target model performance\?
  
The performance of the model with the two layers only hit 72.86% accuracy, which is not as high as I hoped to achieve\.

3. What steps did you take to try and increase model performance\?
  
To increase the model performance, I added a third hidden layer using the "relu" function and changed the neurons of the three layers to 100, 50, and 20\. In addition to that, I increased the number of epochs from 100 to 200\. However, the accuracy was slightly less than 73%, so I changed the number of neurons back to 80, 30, and 10\. Instead of sticking with the "relu" function, I changed to the "tanh" activation function to accomade the negative values in the dataset as well\. The accuracy of the model is now 72.93%\.

## Summary
Summarize the overall results of the deep learning model\. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation\.
  
The deep learning model only scored up to around a 73% with changing activation funnctions, adding more neuron layers, and increasing the number of epochs\. Improving this model beyond this score, may be more difficult, and require further research\. As an alternative, I would recommend using logistic regression to build the model, because it is more straightforward than neural networks that are prone to overfitting\. There are not that many features, and therefore neural networks may be overcomplicating the data analysis\.
