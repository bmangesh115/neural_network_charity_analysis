# neural_network_charity_analysis

# Overview
The purpose is to analyze funding data to build the neural network model to predict if an organization will be succssful if get funded. 
1. Preprocess data for a neural network model
2. Compile, train, and evaluate the model
3. Optimize the model

## Resources
- Data Source: charity_data.csv
- Software: Jupyter Notebook 4, Python 3.7.13, Visual Studio Code 1.68.1

## Results

The link to the Python Script for the intial model.<br>
[PySpark Script for the intial model](/alphabetsoupcharity.ipynb)<br>

The link to the Python Script for optimizatioon of the model.<br>
[Python Script for optimizatioon of the model](/alphabetsoupcharity_optimzation.ipynb)<br>


### Initial neural network model

- Target variable = 'IS_SUCCESSFUL'
- Feature variables = 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATION', 'ASK_AMT'
- Neither target nor feature variables = 'EIN', 'NAME'

1. Initial model was built by dropping 'EIN' and 'NAME' columns.
2. APPLICATION_TYPE category was replaced to 'Other' if counts are less than 500.
3. CLASSIFICATION category was replaced to 'Other' if counts are less than 1500.
4. Input features = 43.
5. Hidden layers= 2.
6. Nodes for first layer = 30.
7. Nodes for second layer = 15.
8. Activation function for first layer = ReLu.
9. Activation function for second layer = ReLu.
10. Activaiton funciton for output layer = Sigmoidal.
11. Epoch = 50.
12. Loss = 0.56 and Accuracy = 0.73.

### Optmization of neural network model


#### First optmization attempt

1. First attempt optimization model was built by dropping 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'columns.
2. APPLICATION_TYPE category was replaced to 'Other' if counts are less than 50.
3. CLASSIFICATION category was replaced to 'Other' if counts are less than 500.
4. Input features = 42.
5. Hidden layers= 2.
6. Nodes for first layer = 30.
7. Nodes for second layer = 15.
8. Activation function for first layer = ReLu.
9. Activation function for second layer = ReLu.
10. Activaiton funciton for output layer = Sigmoidal.
11. Epoch = 50.
12. Loss = 0.55 and Accuracy = 0.73.

#### Second optmization attempt

1. Second attempt optimization model was built by dropping 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'columns.
2. APPLICATION_TYPE category was replaced to 'Other' if counts are less than 50.
3. CLASSIFICATION category was replaced to 'Other' if counts are less than 500.
4. Input features = 42.
5. Hidden layers= 3.
6. Nodes for first layer = 30.
7. Nodes for second layer = 15.
8. Nodes for third layer = 7
9. Activation function for first layer = ReLu.
10. Activation function for second layer = ReLu.
11. Activation function for third layer = ReLu.
12. Activaiton funciton for output layer = Sigmoidal.
13. Epoch = 50.
14. Loss = 0.56 and Accuracy = 0.72.

#### Third optmization attempt

1. Third attempt optimization model was built by dropping 'EIN', 'NAME', 'STATUS', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'columns.
2. APPLICATION_TYPE category was replaced to 'Other' if counts are less than 50.
3. CLASSIFICATION category was replaced to 'Other' if counts are less than 500.
4. Input features = 42.
5. Hidden layers= 3.
6. Nodes for first layer = 30.
7. Nodes for second layer = 15.
8. Nodes for third layer = 7
9. Activation function for first layer = ReLu.
10. Activation function for second layer = ReLu.
11. Activation function for third layer = ReLu.
12. Activaiton funciton for output layer = tanh.
13. Epoch = 50.
14. Loss = 0.57 and Accuracy = 0.72.

## Summary

1. Initial neural network model was built and three attempts were made to optimize model.
3. Optimization focus was on dropping columns, increasing number of bins, adding hidden layer, and using diiferent activation functions.
3. Maximum accuracy achieved was 0.73 with loss of 0.56.
4. For further optimization number of neurons per layer and number of epoch may be increased.