# Neural Network Charity Analysis

The purpose of this analysis is to use features in the provided dataset (charity_data.csv) to create a binary classifier that predicts whether applicants will be successful if funded by Alphabet Soup. 

A neural network was employed to easily handle the data set containing over 34,000 data points. Before the network could be employed, the data was preprocessed to rid it of unnecessary information and null values. After the learning process was ran, the neural network was then tested against our test data which had been split from the training set. The network and data were then tweaked to achieve a higher accuracy in predicting success.

## Results 

### Data Preprocessing

The target variable for which we want the model to predict is labeled as “IS_SUCCESSFUL” in the data frame. This is simply a binary data point that represents success with a 1 and failure with a 0. As the target variable, this is the value which the model will try and predict. All other variables are considered features of the data and describe each case, helping the model learn.

Picture

Variables which add no value to the data (such as “EIN” and “NAME”) were immediately removed so as not to clutter the model with unneeded information. When optimizing the model, many more variables were removed to increase accuracy but there will be more on that later.

###
