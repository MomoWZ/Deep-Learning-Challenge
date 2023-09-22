## Alphabet Soup Chairty Project

## Overview
I've created a model for the Alphabet Soup foundation, it will help to select applicants for funding with the best optimizes chance of success. Using neural networks, I have used the  provided dataset to create a model that can predict whether the applicants will be successful funded by Alphabet Soup. This model designed with 75% accuracy to predict applicant success once funded.

## Results
### Data Processing
This model designed to predict applicant success once funded. I have set the tagered variable as the `IS_SUCCESSFUL` columns in the database. <br>
The frautures variables are the rest columns after droping non-relative columns: `EIN` and `NAME`. <br>
Then, I find the categorical columns:`APPLICAION_TYPE` and `CLASSIFICATION` and started to buketing them. `Others` is created to bin them together.<br>
Moeover, I have transformed all the categorical data to numercial values. Then the data are splited into train data and test data. After creating standard scaler, I use fit the scaler to the data.

### Compiling, Training, and Evaluating the Model
### Optimization -1
For my initial model, I use 3 layers. The total number of neurons are between 2-3 times the number of input features. I started the epochs with 100.
* input layer with 80 neurons, with `relu` activiation function
* second layer with 30 neurons, with `relu` activiation function
* output layer with 1 neuron, with `sigmoid` activiation function
The accuracy is 73% for the testing data, and no sense of overfitting or underfitting.

### Optimization -2
For the second model, I have tried `hidden_nodes_layer1=60, hidden_nodes_layer2=30` with 20 ecophs. And I am taking the chance with `tanh` activiation function. This has provided a 72.4%.

### Optimization -3
I have used Kerastuner `hp.choice` to decide the activation function among `relu`, `tanh`, `sigmod`. I alsoused the hyperparameter tuning with the maximum 50 epochs.
The results is blew with 73.2% accuracy.
`{'activation': 'tanh', <br>
 'first_units': 61,<br>
 'num_layers': 3,<br>
 'units_0': 11,<br>
 'units_1': 11,<br>
 'units_2': 6,<br>
 'units_3': 16,<br>
 'units_4': 11,<br>
 'tuner/epochs': 17,<br>
 'tuner/initial_epoch': 0,<br>
 'tuner/bracket': 1,<br>
 'tuner/round': 0}`
 
## Summary
Given my inability to achieve my target accuracy of 75%, I would not recommend any of the above models.I do believe that making changes to the input layers, trying various activation functions, and ecophs will also help optimize the model and achieve the desired goal of 75% accuracy.
