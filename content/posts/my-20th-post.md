---
title: "Machine Learning - building a model"
date: 2017-10-21T20:36:47+01:00
draft: true
---

### This exercise makes a prediction suing the Titanic data set on a survival of a passenger, following the steps presented in a blog below:

https://medium.com/simple-ai/pandas-library-in-a-nutshell-intro-to-machine-learning-3-acbd39ec5c9c


---


#### 1. First of all we import 2 data sets: a training data set which contains the column 'Survived' and a testing data set which does not contain a column 'Survived - our aim is to predict the survival of the passenger.

```
train = pd.read_csv('C:/Users/Gabi/IdeaProjects/Machine_Learning/train.csv')

train.head()
```

![alt text](/images/ch25.png)



```
test = pd.read_csv ('C:/Users/Gabi/IdeaProjects/Machine_Learning/test.csv'  ) 

test.head()
```

![alt text](/images/ch26.png)


#### 2. We then prepare the data for the analysis by completing the following tasks:

a) filling out the empty data cells and/or (NaN values)

```
train['Embarked']=train['Embarked'].fillna('S')

test['Fare']=test['Fare'].fillna(test['Fare'].median())

test['Age']=test['Age'].fillna(test['Fare'].mean())
train['Age']=train['Age'].fillna(train['Age'].mean())

```


b) enumarating categorical values as ML models only understand numbers

```
train.loc[train['Sex']=='male', 'Sex']=0
train.loc[train['Sex']=='female', 'Sex']=1

test.loc[test['Sex']=='male', 'Sex']=0
test.loc[test['Sex']=='female', 'Sex']=1

train.loc[train['Embarked']=='S', 'Embarked']=0
train.loc[train['Embarked']=='C', 'Embarked']=1
train.loc[train['Embarked']=='C148', 'Embarked']=1
train.loc[train['Embarked']=='Q', 'Embarked']=2

test.loc[test['Embarked']=='S', 'Embarked']=0
test.loc[test['Embarked']=='C', 'Embarked']=1
test.loc[test['Embarked']=='C148', 'Embarked']=1
test.loc[test['Embarked']=='Q', 'Embarked']=2

```


#### 3. Finally, we implement the model which uses the Decision Tree algorithm. 

_The general motive of using Decision Tree is to create a training model which can use to predict class or value of target variables by learning decision rules inferred from prior data(training data)_


_The decision tree algorithm tries to solve the problem, by using tree representation. Each internal node of the tree corresponds to an attribute, and each leaf node corresponds to a class label_



```
X = train.drop(['Survived'], axis = 1)                                                                                                
```

_'Survived' column is removed from axis X as we want to predict the target variable y_


```
y = train['Survived']                                                                                                                                                   
```

```
from sklearn.tree import DecisionTreeClassifier                                 
```


```
model = DecisionTreeClassifier()                                                   
```

The model is fitted below:


```
model.fit(X, y)                                                   
```


We the attempt to get a score for the prediction - ie., we aim to see how accurate the prediction is in comparison to the test data:

```
cross_val_score(model, X, y, cv=10, scoring = 'accuracy').mean())
```

Unfortunately, the following error occurs:

![alt text](/images/ch27.png)

The following line was used to resolve the error, however, it was not successful:

```
train.loc[train['Embarked']=='C148', 'Embarked']=1
```	



		
