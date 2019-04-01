@@@@Data Mining using  classification@@@

# Background
This project aims at practicing data mining using clustering and classification algoritgms. I used the Titanic data set which has been used on Kaggle (https://www.kaggle.com/broaniki/titanic) as the basis for classification method to analyze the relationship between the predictors and passengers¡¯ survival probability, and how to choose the most significant ones to build the model. When it comes to clustering part, I used Trip Advisor Reviews data set which is from (https:// archive.ics.uci.edu/ml/datasets/Travel+Reviews), which is a web site hosted at the University of California at Irvine (UCI) that contains a large number of data sets which people use for testing data mining methods. I used multiple clustering methods in this part to category the 10 attributes for the clustering model.

#Important Note:

Moving forward, this part involves which questions have been answered during the modeling process for the two different data sets.

#What to read for Titanic:
Note: the steps I conducted below involve data cleaning, building the model, estimatation and plotting...

1.Data overview ** 
I used the function below to generate train and test set. And then select the ¡°survived¡± factor to be 1 or 0 to calculate the number in female, male and children who died or survived.
x_train, x_test, y_train, y_test = train_test_split(predictors, target, test_size = 0.10, random_state = 0).

2.Balanced ** 
Details are explained in the report for answering why I think the train and test data are balanced.

3.Decision Tree ** 
After doing the feature engineering, I transfer the numeric features into categorical numeric features. Then I used the code below to library the method I need to build a decision tree,here I choose ["Pclass","Sex"] to be the two attributes for model:

#from sklearn.tree import DecisionTreeClassifier
#from sklearn.metrics import accuracy_score
#col_n = ["Pclass","Sex"]
#x_train = pd.DataFrame(train,columns = col_n)
#y_train = train['Survived']
#decisiontree = DecisionTreeClassifier()
#decisiontree.fit(x_train, y_train)

4.Logistic Regression ** 
Logistic regression is also a good algorithm to do prediction. The ways to test the performance of the prediction model on the test data is also the accuracy score and confusion matrix. Then I finally used the code below to generate the data I want for which I chose ["Pclass","Sex","Age","Fare","Embarked"] to be the predictors and then I library the method to build the logistic model and ROC curve. 

#from sklearn.linear_model import LogisticRegression
#from sklearn.metrics import roc_curve, auc
#col_n = ["Pclass","Sex","Age","Fare","Embarked"]
#x_train = pd.DataFrame(train,columns = col_n)
#x_val = pd.DataFrame(test,columns = col_n)
#logreg = LogisticRegression()
#logreg.fit(x_train, y_train)

5.Linear Regression ** 
For linear Regression, I used the data[¡®Fare¡¯, ¡®Age¡¯]. I do the Age regression based on Fare.
The libraries I used for modeling, measurement and plotting are below.

# from sklearn.linear_model import LinearRegression
#from sklearn.metrics import mean_squared_error, r2_score
# import matplotlib.pyplot as plot





