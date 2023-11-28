# deep-learning-report:

## Perpuse of this analysis: 
"The primary goal of this project is to design and implement an algorithm employing machine learning and neural networks. The specific aim is to develop a predictive model that can assess the likelihood of success for applicants seeking funding from the fictional non-profit foundation, Alphabet Soup. Through the utilization of advanced computational techniques, our goal is to provide valuable insights that assist in the decision-making process, optimizing the foundation's support for prospective projects and fostering overall success within its mission."

## Data Preprocessing

I was given a CSV file ontaining more than 34,000 organizations that have received funding from Alphabet Soup over the years that I read into Pandas. 

* dropping the non-beneficial ID columns, 'EIN' and 'NAME'.,
* finding the number of data points for each unique value for each of the columns that had more than 10 unique values - `APPLICATION_TYPE` and `CLASSIFICATION`,
* choosing a cutoff point of 725 and 1918, respectively, to bin rare categorical values together into a new value called "Other",
* using `pd.get_dummies()` to convert categorical data to numeric,
* dividing `the data into a target array (IS_SUCCESSFUL) and features arrays,
* applying the `train_test_split` to create a testing and a training dataset,
* using `StandardScaler` to scale the training and testing sets
  
As a result data included 44 features. The target variable (y) was `IS_SUCCESSFUL`. Then I split The data into training and test subsets.

## Compiling, Training, and Evaluating the Model
The model was required to achieve a target predictive accuracy higher than 75%.  My first model got me to the point of accuracy rate 72.60% . I had to make  a few official attempts using machine learning and neural networks.

* Results: 
  
Model #1: (AlphabetSoupCharity.h5) resulted in an accuracy score of 72.6%.  This means that 72.6 % of the model’s predicted values align with the dataset’s true values.

What I used:

layers = 2
layer1 = 9  neurons : activation function = ‘relu’
layer2 = 5 neurons : activation function = ‘relu'
epochs = 100


Model #2: (AlphabetSoupCharity.Optimization.h5) resulted in an accuracy score of 75.27%. I added another layer and neurons. This attempt resulted in an accuracy score of 75.27%. This means that 75.27% of the model’s he highest accuracy score of the two models. This means that both models's predicted values align with dataset's true values . By adding layers and neurons I increased model performance.  


layers = 3
layer1 = 10 neurons : activation function = ‘relu’
layer2 = 8 neurons : activation function = sigmoid"'
layer3 = 6 neurons : activation function = 'sigmoid'
epochs = 30

## Summary: 

In both trials, the model successfully reached a predictive accuracy of 75%, indicating a notable improvement. Consequently, I would deem this outcome as meeting our targeted goal.