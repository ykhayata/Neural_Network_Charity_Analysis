# Neural Network Charity Analysis

## Overview

The main purpose of my analysis is to leverage a neural network to help us determine whether or not companies should recieve loans from Alphabet Soup. Throughout this analysis, we use python's TensorFlow library to create, train, and evaluate the data gathered from previous loans.

## Our Results

### Date Preprocessing 

Our target variable is the "IS_SUCCESSFUL" column, so we were forced to remove the "EIN" and "NAME" columns because they simply did not offer us any useful data that would improve the accuracy of the model. The remaining columns then became the features for the model.

### Compiling, Training, and Evaluating the Model

We started off with adding the relu activation functions to the first two layers, while the output layer had a sigmoid activation function. We chose this method of work because relu better alligns with nonlinear data, while implementing two layers allows for a second layer to reweight the inputs from the first layer. 

In our second attempt on improving accuracy, we went ahead and lowered the threshold for the classification column so we see more unique values. We also added a third layer with 6 neurons. See results below: 

<img width="615" alt="v1" src="https://user-images.githubusercontent.com/74481469/114342922-a9c5e480-9b11-11eb-8c01-10a183d3f643.png">

In our 3rd attempt, we reverted back to the previous threshold and changed the activation function for the three layers to "tanh". Please see results below:

<img width="902" alt="v2" src="https://user-images.githubusercontent.com/74481469/114343020-ded23700-9b11-11eb-98db-bc5a9fdab418.png">

In our final attempt, we removed the whole "STATUS" column, and reverted back to two layers and the relu activation function. We also wanted to experiment increasing the paramaters passed from the first layer to second layer so we increased paramters from 54 to 104. Please see below:

<img width="540" alt="v3" src="https://user-images.githubusercontent.com/74481469/114343157-2fe22b00-9b12-11eb-87c6-66a6d60c95c5.png">

## Summary

Unfortunately, we were unable to create a model that performed at 75% accuracy after numerous attempts. If I were to try this again, I would dive deeper into activation functions so I can correctly match each function with its corresponding data. Once we do this, the accuracy of the model is bound to increase. 
