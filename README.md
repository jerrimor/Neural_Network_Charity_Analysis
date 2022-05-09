# Neural_Network_Charity_Analysis

## Overview of Analysis
The analysis was to help the company, Alphabet Soup determine if a candidate will be successful with receiving funds from them.  The dataset provided had an enormous amount of metadata about each organization, such as:
  EIN and NAME—Identification columns
  APPLICATION_TYPE—Alphabet Soup application type
  AFFILIATION—Affiliated sector of industry
  CLASSIFICATION—Government organization classification
  USE_CASE—Use case for funding
  ORGANIZATION—Organization type
  STATUS—Active status
  INCOME_AMT—Income classification
  SPECIAL_CONSIDERATIONS—Special consideration for application
  ASK_AMT—Funding amount requested
  IS_SUCCESSFUL—Was the money used effectively

The initial model run didn't provide an accuracy that was good enough so three other attempts were created and run to hopefully increase the accuracy.  


## Results

- Data Preprocessing 
  The two columns that were removed in cleaning the data were EIN and NAME.  Those two columns didn't add value for this analysis.  Another preprocessing step was to bin APPLICATION_TYPE and categorize any of the types that were less than 500 records.  We put those into an 'Other' category.  
  The column, IS_SUCCESSFUL, is a target variable.  
  All the other variables were the features. 
  
- Compiling, Training, Evaluating Model
  How many neurons, layers, and activation functions did you select for your neural network model, and why?
  The initial model had 2 hidden layers and 1 output layer. 
    - The first layer had 80 neurons and 80 bias terms. 
    - The second layer had 30 neurons and 30 bias terms.
    - The output layer had 30 inputs, 1 neuron and 1 bias term. 
    - The target performance was greater than 75%.  This model only achieved 72.3%
    - 
![DD43E20B-4A8D-4005-A361-7DB65BCE61F6_4_5005_c](https://user-images.githubusercontent.com/96222437/167340757-a862d464-0249-43f5-828d-8b5820e39d3a.jpeg)

 


I attempted three times to improve that initial model's accuracy.  I did not achieve 75%.  
In the first attempt, I added binning to the AFFILIATION.  I wanted to put smaller values into an other category, it was for anything less than 50.  
this did not achieve 75% however I did get to 72.5%.

![6EFB5163-6F8B-4045-938A-F473E66CF884](https://user-images.githubusercontent.com/96222437/167340345-8b3ce76c-5293-4aab-ad14-cdc4b0793dc4.jpeg)


In the second attempt, I increased the neurons to 100 in the first layer and 50 in the second layer.  
This did not achieve 75%.  It only achieved 72.6%


![136340B4-9601-4727-BFAA-57AB56C83EFC_4_5005_c](https://user-images.githubusercontent.com/96222437/167340665-72df68ac-2ed7-4c20-bb0d-b33f746e3ed2.jpeg)


In the third attempt, I added another hidden layer so that the third layer had a neuron count of 30, while the first had 100 and the second 50.  I also adjusted the epochs to 75.  These changes did not hit 75% either.  Instead it only hit 72.5% again.

![114F0C93-AF7A-438F-ACCA-F0D5054FFDF1](https://user-images.githubusercontent.com/96222437/167340407-bea2e4dc-6e33-461b-bb84-836d674a3125.jpeg)



## Summary

The elimination of categories within the features did add some improvement however in this model, adding another layer did not make much change.  The model should be run further with perhaps another model type to see if the accuracy could be increased.  The models as is are not too far off from the target and so this may be okay for this type of risk taking.  
