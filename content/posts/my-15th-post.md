---
title: "Student sleep data"
date: 2017-10-03T07:28:14+01:00
draft: true
---

A data set which show the effect of two soporific drugs (increase in hours
of sleep compared to control) on 10 patients. 

Data source is listed below:

https://vincentarelbundock.github.io/Rdatasets/datasets.html

A line of code below is used to create a data frame:

```
data = pd.read_csv('sleep.csv')
```


In order to explore the first 6 lines of data, we use the method below:

```
data.head()
```

The following line of code produces descriptive statistics of the data set:

```
data.describe()
```

It suggests that out data set contains 20 lines of data and 4 columns. 
