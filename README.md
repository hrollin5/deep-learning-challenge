# Deep Learning Challenge
This project highlights the following technical skills:
* Data Manipulation
* Machine-Learning: Neural Networks
* Keras Tuner
* Exploratory Data Analysis
* Model Evaluation
* Version Control

## Objective
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

### Data
From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.
Data were accessed accessed November 09, 2023. Data for this dataset was generated by edX Boot Camps LLC. 

The data provided included the following variables:
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


### Technologies Used
* Numpy
* Python
* Sk Learn
* Pandas
* TensorFlow

## Results

### Compiling, Training, and Evaluating the Model

After using the Keras Tuner, I determined the best model would have initially 100 neurons, 2 layers with 45 and 35 neurons, with tahn activation. 

I was able to achieve target performance. Ultimately, my model scored 79.0% accuracy. 

To increase performance of the model, I ran a Keras Tuner to help select the more accurate model parameters. I also lowered the threshold for binning the classification and application type parameters to allow more variance in the data. When I still could not improve the model accuracy, I investigated the Name variable further. The names were not, in fact, unique to each project. I added the name data back in and binned them to have any with fewer than 6 rows (venture) as other. 

<img width="727" alt="Screenshot 2023-11-09 at 10 38 12 PM" src="https://github.com/hrollin5/deep-learning-challenge/assets/130103105/8d3eec37-32dd-4c5e-9963-065e7e1ac670">


