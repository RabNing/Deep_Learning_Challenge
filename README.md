# Deep Learning Model Performance Report

## Overview
Alphabet Soup, a nonprofit foundation, seeks to identify successful applicants for funding using machine learning and neural networks. They provide a dataset of over 34,000 organizations that received funding. The goal is to create a binary classifier using TensorFlow, predicting an organization's success if funded by Alphabet Soup. After the initial model is set up, optimize the model using various methods to achieve a predictive accuracy above 75%.

## Results
### Data Preprocessing
- What variable(s) are the target(s) for your model?
  - The target variables of the model are data in the column of IS_SUCCESSFUL, which indicates if the money was used effectively
- What variable(s) are the features for your model?
  - Data in the other columns other than the target variable are features, such as APPLICATION_TYPE, CLASSIFICATION, USE_CASE, etc.
- What variable(s) should be removed from the input data because they are neither targets nor features?
  - Identification columns EIN and NAME are removed because they are non-relevant variables to the targets.
  
### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - In the initial model, I select 3 hidden layers and include 80 neurons on the 1st layer, 30 neurons on the 2nd layer, and 1 neuron on the last output layer. In this way, I ensure that the total number of neurons in the model is a bit more than 2 times the number of 
  input features. I select the relu activation function for the first and second layers, and the sigmoid activation function for the 
  output layer because the goal is to predict binary classification.  
- Were you able to achieve the target model performance?
  - I trained the model for 100 epochs and achieved an accuracy score of 72.6% for the testing data.
- What steps did you take in your attempts to increase model performance?
  - Beyond the initial model, I continued to try 3 different methods to optimize the model for a higher accuracy score. Unfortunately, 
  none of the 3 optimization models was able to achieve an accuracy score that was higher than 75%. The 3 methods I tried are :
    - Dropping one more non-relevant feature column 'Status'
    - Modify the number of values for each bin
    - Adding more neurons to the first 2 hidden layers and changing the activation function to the last layer. 
## Summary
As both the initial model and optimized models couldn't achieve an accuracy score that is higher than 75%, I would not recommend using any of these models for prediction. If I have a chance to use a different model to solve this problem, in addition to experimenting with numbers of hidden layers, neurons, and activation functions, I will also do more steps in processing the input data, trying to identify and get rid of potential outliers.
