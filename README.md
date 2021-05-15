# Neural Network Charity Analysis

The purpose of this analysis is to use features in the provided dataset (charity_data.csv) to create a binary classifier that predicts whether applicants will be successful if funded by Alphabet Soup. 

A neural network was employed to easily handle the data set containing over 34,000 data points. Before the network could be employed, the data was preprocessed to rid it of unnecessary information and null values. After the learning process was ran, the neural network was then tested against our test data which had been split from the training set. The network and data were then tweaked to achieve a higher accuracy in predicting success.

## Results 

### Data Preprocessing

The target variable for which we want the model to predict is labeled as “IS_SUCCESSFUL” in the data frame. This is simply a binary data point that represents success with a 1 and failure with a 0. As the target variable, this is the value which the model will try and predict. All other variables are considered features of the data and describe each case, helping the model learn.

Picture

Variables which add no value to the data (such as “EIN” and “NAME”) were immediately removed so as not to clutter the model with unneeded information. When optimizing the model, many more variables were removed to increase accuracy but there will be more on that later.

Categories with low values in columns such as “APPLICATION_TYPE” and “CLASSIFICATION” were lumped into and “Other” category in order to work towards a nice easy to read data frame. OneHotEncoder was then implemented to make split these columns apart to columns of their respective categories which were then binary. 

Pic

### Compiling, Training, and Evaluating the Model

The target model performance was 75% accuracy, which I fell just short of at what?. This was improved over the starting accuracy of about 62%.

To optimize the model, many different neural networks were run on several different iterations of the data set. Removing columns such as affiliation and application type had no significant effect on the model’s accuracy. One variable which did yield an improved accuracy was “ASK_AMT”, the amount of money the applicant had asked for. This variable was left out of our final model.

Adding additional layers and neurons to the model at times hurt the accuracy (probably due to overfitting) while at other times offered no significant improvement. Our original model consisted of 2 layers with 80 and 30 neurons, respectively. This was increased to a most of 3 layers with 100, 60 and 30 neurons. The highest accuracy came from using 2 layers with 80 and 40 neurons. 

The activation function was also changed from Rectified Linear Unit (ReLU) to a sigmoid function to increase the model’s accuracy. The ReLU function works well with non-linear data but in this case of a binary target, the sigmoid function performed much better. 


