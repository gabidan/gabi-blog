---
title: "Time use analysis"
date: 2017-09-21T07:31:30+01:00
draft: true
---


This data explores how people spend their time depending on country and sex, with activities such as paid work, household and family care, etc.


Data source is listed below:


https://perso.telecom-paristech.fr/eagan/class/igr204/datasets 


CSV file was uploaded into pandas using the following line of code and a data frame  was created :

```
data = pd.read_csv('timeuse.csv')
```


Using the line of code below we explore the first couple of lines of the data frame, and receive a summary of it:

```
data.head()
```

![alt text](/images/ch9.png)


As this data set contains 58 columns, a smaller data frame is created using the following line of code:

```
data1 = data[['SEX','Sleep']]
```

--- 


The line of code below generates the descriptive statistics of the new data frame. Analyzes both: numberic and objective series. 

```
data1.describe(include = 'all')
```

![alt text](/images/ch10.png)


**Numerical analysis**

