# Neural Network Charity Analysis

## Overview

The purpose of this analysis is to predict if charitable organizations will be successful if they receive funding from Alphabet Soup.

## Results

- Data Preprocessing

  - What variable(s) are considered the target(s) for your model?
 
    The IS_SUCCESSFUL column determines whether the donation was used effectively and is considered the target of this model.
  
  - What variable(s) are considered to be the features for your model?
 
    The APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns are the features.
    
  - What variable(s) are neither targets nor features, and should be removed from the input data?

    EIN and NAME are considered identification information and should be removed from the input data.
    

- Compiling, Training, and Evaluating the Model

  - How many neurons, layers, and activation functions did you select for your neural network model, and why?

    This model is made up of two hidden layers with 100 and 30 neurons and each layer activated by reLU.  The Output layer activation is sigmoid.  To compile the model, the loss function that was used is binary crossentropy and the optimizer was adam.  
  - Were you able to achieve the target model performance?

    No.  None of my models achieved greater than 75% accuracy.  
    
    
  - What steps did you take to try and increase model performance?

    The first attempt I made was to try binning the ASK_AMT into fewer buckets, along with APPLICATION_TYPE and CLASSIFICATION.  
    
      ![first test](https://user-images.githubusercontent.com/95720986/167314277-cb5c844e-a941-4737-9af4-e52542ab6393.png)

    The second attempt I added a third hidden layer.

      ![second test](https://user-images.githubusercontent.com/95720986/167314339-663e7d41-3873-4135-8c2e-65126bddcfd7.png)

    The third attempt I kept the three hidden layers but changed the activation from reLU to tanh.
    
        ![third test](https://user-images.githubusercontent.com/95720986/167314395-18d45f6a-aece-4f94-ad12-9700796fb505.png)

## Summary
