---
title: "Head Dimensions in Brothers"
date: 2017-09-19T18:51:09+01:00
draft: true
---

The data consist of measurements of the length and breadth of the heads of 
pairs of adult brothers in 25 randomly sampled families.  All measurements
are expressed in millimetres.


The data was extracting from the folowing website:

https://vincentarelbundock.github.io/Rdatasets/datasets.html

The following line of code was used to import the data into Pandas and build a data frame:

```
data = pd.read_csv('frets.csv')
```


The line of code below was used to explore data headline:

```
data = data.head(5)
```

The outcome (the first 5 lines of the data frame) is below:


![alt text](/images/frets.png)