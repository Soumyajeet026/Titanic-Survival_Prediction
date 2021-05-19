# Titanic-Survival_Prediction
At first I read the two files train.csv and test.csv and kept them in two different data frames. 
Then I have discarded 4 attributes 'PassengerId', 'Name', 'Ticket', 'Cabin' as the survival of a person is totally independent of them, intuitively ,for both the  data frames.
I have one hot encoded the 'Sex' and 'Embarked' attributes for both the data frames.
I have replaced the NaN values of 'Sex' and 'Embarked' attributes with the median values of the respective attributes for both the data frames.
Then grouped the 'Age' column into 6 parts and put values 1,2,3,4,5,6 accordingly.
I scaled the 'Fare' column into the range (0,1).
Then I did a 10 fold cross validation over the training data frame for Logistic Regression,Support Vector Machine(Linear and Rbf kernel),K Nearest Neighbour,Decision Tree,Random Forest, Perceptron and Bayes Classifier.
Highest accuracy was obtained with Support Vector Machine Rbf kernel function and so I predicted the survival of the persons in the test data frame and kept it in Predicted_Survived.csv file with the 'PassengerId' column. 
