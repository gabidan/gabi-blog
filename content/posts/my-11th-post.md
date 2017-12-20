---
title: "Attributes of Animals"
date: 2017-09-26T21:24:07+01:00
draft: true
---

![alt text](/images/mystical.jpg)


### This data set considers 6 binary attributes for 20 animals


The data was extracted from the folowing website:

https://vincentarelbundock.github.io/Rdatasets/datasets.html

The line of code below was used to import the data into Pandas and build a data frame:

```
data = pd.read_csv('animals.csv')
```

The first 5 lines of the data frame were explored using the following line of code:

```
data.head()
```


In order to explore the basic features, summary and measures of the data Pandas 'describe' method was used:

```
data.describe(include='all')
```

**_(include='all')_** - *allows to analyse both - numerical and non-numerical data*




**Numerical analysis**

The line of code below groups the data of a selected column into intervals represented on axis X. The frequency of data belonging to that interval is represented on axis Y.

```
data['fly'].hist()
```


![alt text](/images/ch11.png)



*as this data is binary, the graph above suggests that animals belonging to the interval up to 1.2 do not posess the chosen feature, and animals plotted in the interval between 1.8 and 2 - do posess the chosen feature* 

