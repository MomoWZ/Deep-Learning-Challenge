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

## Summary
