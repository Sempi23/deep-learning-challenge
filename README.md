# Deep-Learning-Challenge
Alphabet Soup Funding Analysis

## Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. In this project, we shall use machine learning and neural networks, on the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

The CSV received contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

 - EIN and NAME—Identification columns
 - APPLICATION_TYPE—Alphabet Soup application type
 - AFFILIATION—Affiliated sector of industry
 - CLASSIFICATION—Government organization classification
 - USE_CASE—Use case for funding
 - ORGANIZATION—Organization type
 - STATUS—Active status
 - INCOME_AMT—Income classification
 - SPECIAL_CONSIDERATIONS—Special considerations for application
 - ASK_AMT—Funding amount requested
 - IS_SUCCESSFUL—Was the money used effectively

 ## Analysis
 Step 1: Data Preprocessing:

 - Non-beneficial columns dropped
 - cut offs established for features that had many unique values
 - categorical data converted to numeric
 - preprocessed data split into features array (x), and target array (y)
  - train_test_split function used to split the data into training and testing datasets
  - using StandardScaler to scale the training and testing sets

Step 2: Compile, Train, and Evaluate the Model:

   - creation of a neural network model using TensorFlow and Keras
   - Compilation and training the model using various input layers and appropriate activation functions
   - evaluation of the model using the test data to determine loss and accuracy
   - save model


Step 3: Model Optimization:

Optimize model to achieve a target predictive accuracy higher than 75%

## Results

1.  The target variable in all models was 'IS_SUCCESSFUL' (1 = applicant successful, 0= applicant not successful).



2. Neural Network Model 1:

 - Features: APPLICATION_TYPE, AFFILIATION,	CLASSIFICATION,	USE_CASE,	ORGANIZATION,	STATUS,	INCOME_AMT,	SPECIAL_CONSIDERATIONS, and	ASK_AMT.
 - Non-beneficial dropped columns: EIN and NAME
 -  2 hidden layer sizes with 80, 30  neurons respectively utilized ReLU activation function with 100 training epochs
 - Accuracy score = 0.7303
 - Loss = 0.5634

    - This model was not able to achieve our target score of 75% thus optimization is required.



3. Neural Network Model Optimization 1:

 - Features: APPLICATION_TYPE, AFFILIATION,	CLASSIFICATION,	USE_CASE,	ORGANIZATION, INCOME_AMT,	 and	ASK_AMT.
 - An additional two Non-beneficial dropped columns: EIN, NAME, STATUS,and SPECIAL_CONSIDERATIONS
 - 2 hidden layer sizes with 100, 50  increased neurons respectively, utilized ReLU activation function with 100 training epochs
 - Accuracy score = 0.729
 
    - This model was still not able to achieve our target score of 75% thus optimization is required.



4. Neural Network Model Optimization 2:

- Features: APPLICATION_TYPE, AFFILIATION,	CLASSIFICATION,	USE_CASE,	ORGANIZATION, INCOME_AMT,	 and	ASK_AMT.
- An additional two Non-beneficial dropped columns: EIN, NAME, STATUS,and SPECIAL_CONSIDERATIONS
- increased to 4 hidden layer sizes with 80, 30, 20, 10  neurons respectively, utilized ReLU activation function.
- increased to 200 training epochs
- Accuracy score = 0.7303
- Loss = 0.6037

    - This model was still not able to achieve our target score of 75%


## Summary

All the three models produced similar accuracy score of ~73%. They following methods were used to attempt to increase accuracy score to >=75%:

    i. Dropping an additional 2 columns
    ii. Increasing number of neurons
    iii. increasing hidden layers from 2 to 4
    iv. increasing number of epochs from 100 to 200

 For further optimization i would consider using another activation function such as tanh on the hidden layers. If  that didn't suffice i would try and create more bins for rare occurences in columns or increase or decrease the number of values of each bin.  


 ## References
 
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.





