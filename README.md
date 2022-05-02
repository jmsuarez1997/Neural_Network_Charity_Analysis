# Neural_Network_Charity_Analysis

## Overview of the analysis:
This a neural network analysis built with Python and the Pandas, TensorFlow, StandardScaler, and Train Test Split libraries. The analysis uses data from more than 34,000 organizations that have recived charitable funding from Alphabet Soup and a neural network model to pridict if applicants will be successful if funded. The following are columns within the charity_data.csv that capture metadata about each organization:

- **EIN** and **NAME—Identification** columns
- **APPLICATION_TYPE**—Alphabet Soup application type
- **AFFILIATION**—Affiliated sector of industry
- **CLASSIFICATION**—Government organization classification
- **USE_CASE**—Use case for funding
- **ORGANIZATION**—Organization type
- **STATUS**—Active status
- **INCOME_AMT**—Income classification
- **SPECIAL_CONSIDERATIONS**—Special consideration for application
- **ASK_AMT**—Funding amount requested
- **IS_SUCCESSFUL**—Was the money used effectively

## Results:
Using bulleted lists and images to support your answers, address the following questions.

**Data Preprocessing**
- IS_SUCCESSFUL is the target column of our model. This column indicates whether an organization used the donation effectively or not.  

- The model features are APPLICATION_TYPE, CLASSIFICATION, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, IS_SUCCESSFUL, USE_CASE, and AFFILIATION. 

- EIN and Name are identification columns and are removed from the data set. 

**Compiling, Training, and Evaluating the Model**
- There are a total of 110 neurons and two layers. Relu is the layer's activation function, and sigmoid is the output layer.  
I could not get this model to reach 75 % accuracy. The best the model could get to was 69%. 
- I tried several steps to optimize the model, and the only attempt that worked was increasing the number of neurons in the hidden layer. The following are steps I took to optimize the model: 
    - dropping columns USE_CASE and AFFILIATION. 
    - added a third layer to the model. 
    - increased the number of counts to replace/increase CLASSIFICATION and APPLICATION_TYPE's "Other" column. 
    - changed the activation function to `tanh`
## Summary:

The deep learning model did not reach the target of 75% accuracy. After trying a few attempts to optimize the function, the best result was 69.39 % accuracy. Since this is a binary problem (successful vs. not successful), I recommend trying a logistic regression algorithm to perform binary classification. I would then try to optimize the accuracy by dropping columns that are not indicators of success. 