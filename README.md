# Neural Network - Charity Analysis

### Overview

In this project, we will help Beks to create a binary classifier model that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. We will also try to optimize and improve model to see if accuracy can be improved. We have CSV containing more than 34,000 organizations that have received funding from Alphabet soup over the years. Here are the columns which that capture metadata about each organization.

- **EIN** and **NAME**—Identification columns
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

### Results

#### Data Preprocessing

- What variable(s) are considered the target(s) for your model?
  - **IS_SUCCESSFUL** is target variable for the model.

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/6.png?raw=true)

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/7.png?raw=true)

- What variable(s) are considered to be the features for your model?
  - **APPLICATION_TYPE**, **AFFILIATION**, **CLASSIFICATION**, **USE_CASE**, **ORGANIZATION**, **STATUS**, **INCOME_AMT**, **SPECIAL_CONSIDERATIONS**, **ASK_AMT** are features for the model.
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - **EIN** and **NAME** doesn't add any value to the model and can be removed.

#### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - I selected 3 hidden layers, each having 100, 80, 30 neurons respectively. I chose relu activations for input data and sigmoid for output layer becuse it's binary classification problem & those activations works well with those.

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/5.png?raw=true)

- Were you able to achieve the target model performance?
  - I was able to achieve ~73% performance which was lower then 75% target.

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/1.png?raw=true)

- What steps did you take to try and increase model performance?
  - I tried various steps to improve performance as below:
    1. Removed "Status" variable as I felt it was 1 for most of the data and not adding much value.
    2. Tried various activation functions.
    3. Tried various number of neurons and layers.
    4. Changed epochs.

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/2.png?raw=true)

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/3.png?raw=true)

![image](https://github.com/hemalis/Neural_Network_Charity_Analysis/blob/main/images/4.png?raw=true)

### Summary

In Summary, after various steps to improve model performance, I was able to reach at ~73%. We can try different models other then Sequential like random forest and/or change size of the sample data to improve accuracy. We can also try changing split between training and test data to see if it improves further. Overall, model still needs improvements and >75% accuracy can be achieved.
