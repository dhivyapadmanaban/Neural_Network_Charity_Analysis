# Neural_Network_Charity_Analysis

## Project Overview

With the knowledge of machine learning and neural networks,I used the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Source dataset is a csv file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

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

## Results

### Data Preprocessing

Before building ML using neural network, I performed data preprocessing to analyze, clean and scale the data suitable for neural network model.

- **IS_SUCCESSSFUL** column variable is considered as target of this model.
- **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT** variables are the features of the model.
- **EIN** and **NAME** are neither target nor features so they are dropped from the dataset.


###  Compiling, Training, and Evaluating the Model

#### **How many neurons, layers, and activation functions are selected for the model?**

I used below specifics to train and evaluate neural network model because I would like to start with two hidden layers with recommended activation.

1. Number of hidden layers : 2 
2. Number of neurons in hidden layer 1 : 50
3. Number of neurons in hidden layer 2 : 40
4. Hidden layer activation : RELU
5. Output layer activation : Sigmoid

![image](https://user-images.githubusercontent.com/83181834/133170101-478a4853-7b89-4f9f-ad15-5b8dd638d26e.png)

#### **Target model performance?**

The model was not able to reach the target 75%. The accuracy for my model was 72.5%

![image](https://user-images.githubusercontent.com/83181834/133170360-87a09634-a93f-4a59-ac83-d92addd437a1.png)

#### **Steps taken to increase model performance?**

**Attempt 1:**

For the first attempt, I increased hidden layer to 3 and added more neurons to each layer.

1. Number of hidden layers : 3
2. Number of neurons in hidden layer 1 : 60
3. Number of neurons in hidden layer 2 : 40
4. Number of neurons in hidden layer 3 : 20
5. Hidden layer activation : RELU
6. Output layer activation : Sigmoid

![image](https://user-images.githubusercontent.com/83181834/133170680-59c70a27-fa6e-48d6-96a6-a5c23b4d295e.png)

#### **Target model performance?**

The model was not able to reach the target 75%. The accuracy for my model was 72.7%

![image](https://user-images.githubusercontent.com/83181834/133170727-6a069af0-bce5-47a1-8591-9b27b917a56a.png)


**Attempt 2:**

For the second attempt, I increased the neurons to each layer and change the epoch.

1. Number of hidden layers : 3
2. Number of neurons in hidden layer 1 : 100
3. Number of neurons in hidden layer 2 : 70
4. Number of neurons in hidden layer 3 : 40
5. Hidden layer activation : RELU
6. Output layer activation : Sigmoid

![image](https://user-images.githubusercontent.com/83181834/133170875-31edaf52-97b7-477b-a020-d7e0e7124781.png)

#### **Target model performance?**

The model was not able to reach the target 75%. The accuracy for my model was 72.5 %

![image](https://user-images.githubusercontent.com/83181834/133170917-fc41e538-6300-4a9b-bdb8-745978a5a068.png)


**Attempt 3:**

For the final attempt, I kept the hidden layer and neurons as same but changed the activation function.

1. Number of hidden layers : 3
2. Number of neurons in hidden layer 1 : 100
3. Number of neurons in hidden layer 2 : 70
4. Number of neurons in hidden layer 3 : 40
5. Hidden layer activation : tanh
6. Output layer activation : Sigmoid

![image](https://user-images.githubusercontent.com/83181834/133170989-28810ff1-edbe-43ce-baae-fc59948ad6a4.png)


#### **Target model performance?**

Still, the model was not able to reach the target 75%. The accuracy for my model was 72.6 %.

![image](https://user-images.githubusercontent.com/83181834/133171024-d4ceb88a-4d06-462c-803b-a9c0fc74ef8f.png)


## Summary

After many attempts, model stays in the accuracy range of 72.2 - 72.6 % and not reaching 75% required accuracy. This shows the model is over-fitted, however we can further optimize the mode by additional data to dataset and removing more features and retrain the model.

Since the accuracy is not up to the standard using neural network model we can try applying other ML model like Random Forest classifiers.This model is also appropriate for this binary classification problem and can often perform comparably to deep learning models with just two hidden layers.
