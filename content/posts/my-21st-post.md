---
title: "Iris dataset - applying machine learning models"
date: 2017-10-22T20:09:59+01:00
draft: true
---


![alt text](/images/iris.jpg)


### This exercise applies 6 different algorithms to predict the species of iris using 4 attributes of the flower: sepal-length, sepal-width, petal-length, petal-width.



----



**1. First of all the dataset is explored in a couple of different ways:**

a) Get the idea on the no. of columns and rows:

```
print(dataset.shape)
```


b) Explore the first rows of the dataset:

```
dataset.head()
```

![alt text](/images/ch34.png)


c) Review the statistical summary:

```
dataset.describe()
```


![alt text](/images/ch29.png)


d) Take a look at the number of instances (rows) that belong to each class:

```
print (dataset.groupby('species').size())
```

![alt text](/images/ch30.png)



**2. Visualisations give a basic idea about the data:** 


a) The distribution of attribute measures:

```
dataset.hist()
```


```
plt.show()
```

![alt text](/images/ch32.png)



b) Relationship between the attributes:

```
scatter_matrix(dataset)
```


```
plt.show()
```


![alt text](/images/ch33.png)


**3. The dataset is split into training and test data (80/20)** 


```
array = dataset.values
X = array[:,0:4]
Y = array[:,4]
validation_size = 0.20
seed = 7
X_train, X_validation, Y_train, Y_validation = model_selection.train_test_split(X, Y, test_size=validation_size, random_state=seed)
```


a) 10-fold cross validation is used to estimate accuracy: data is split into 10 parts, 9 parts are usde for training, 1 is used for testing for all combinations of train-test splits.


```
seed=7
scoring = 'accuracy'
```


b) 6 different algorithms will be used:


- Logistic Regression (LR)
- Linear Discriminant Analysis (LDA)
- K-Nearest Neighbors (KNN).
- Classification and Regression Trees (CART).
- Gaussian Naive Bayes (NB).
- Support Vector Machines (SVM)

```
models = []
models.append(('LR', LogisticRegression()))
models.append(('LDA', LinearDiscriminantAnalysis()))
models.append(('KNN', KNeighborsClassifier()))
models.append(('CART', DecisionTreeClassifier()))
models.append(('NB', GaussianNB()))
models.append(('SVM', SVC()))
# evaluate each model in turn
results = []
names = []
for name, model in models:
	kfold = model_selection.KFold(n_splits=10, random_state=seed)
	cv_results = model_selection.cross_val_score(model, X_train, Y_train, cv=kfold, scoring=scoring)
	results.append(cv_results)
	names.append(name)
	msg = "%s: %f (%f)" % (name, cv_results.mean(), cv_results.std())
	print(msg)
```


---



**The output below shows that KNN has the largest estimated accuracy score:***

![alt text](/images/ch35.png)
