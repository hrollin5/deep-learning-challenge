# Neural Network Model to Predict Success of Ventures
## OVERVIEW:
The purpose of this analysis is to predict the outcome of applicant ventures. A neural network machine learning model was developed and optimized to aid in this endeavor. 

## RESULTS:

### Data Preprocessing

The target variable was the binary variable named "IS_SUCCESSFUL". 1 indicates success. 

The feature variables are 
* 'APPLICATION_TYPE': 17 types, narrowed down to the top 8 plus an "Other" category
* 'AFFILIATION': Independent or company sponsored
* 'CLASSIFICATION': 71 classifications, narrowed down to those with over 1000 rows and an "Other" category
* 'USE_CASE': Preservation, Product Development, Community Service, Healthcare, Other
* 'ORGANIZATION': Trust, Association, Co-operative, Corporation
* 'STATUS': Active (1) or inactive (0)
* 'INCOME_AMT': Categorical with ranges of income
* 'SPECIAL_CONSIDERATIONS': Yes or no
* 'ASK_AMT': Continuous numerical

The variables EIN and Name were dropped as they were neither the target nor feature variables. 

### Compiling, Training, and Evaluating the Model

After using the Keras Tuner, I determined the best model would have initially 100 neurons, 2 layers with 45 and 35 neurons, with tahn activation. 

I was able to achieve target performance. Ultimately, my model scored 79.0% accuracy. 

To increase performance of the model, I ran a Keras Tuner to help select the more accurate model parameters. I also lowered the threshold for binning the classification and application type parameters to allow more variance in the data. When I still could not improve the model accuracy, I investigated the Name variable further. The names were not, in fact, unique to each project. I added the name data back in and binned them to have any with fewer than 6 rows (venture) as other. 

### Recommendation for a Different Model

To try for increased accuracy, I would recommend using a random forest model. This model type would be great for our dataset, as Random Forests handle categorical variables well, is an ensemble model (which helps to reduce overfitting and improve the model's generalization to new data) and provides a feature importance score, which can help to interpret the relative importance of different features in predicting the outcome.
