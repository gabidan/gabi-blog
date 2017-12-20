---
title: "Statistics - Correlation"
date: 2017-10-10T22:02:34+01:00
draft: true
---


### Correlation is a statistical term which describes a linear relationship between 2 variables


Always represented by a number between -1 and 1, correlation shows how close the linear relationsho between 2 variables is. 
Varying from Perfect Positive Correlation (1) to Perfect Negative Correlation (-1) the coefficient suggests that variables having positive correlation hold values which increase together. 
Variables whose correlation is negative, hold values which increase in one,  but decrease in another. 


---

**An example presented using Pandas:**

 *1. Sample data frame created:*
	

```
df = DataFrame({'x': [1,2,3], 'y': [1,2,3]})
```


```
df.head()
```

![alt text](/images/ch22.png)


 *2. Correlation coefficient found using the line of code below:*


```
df['x'].corr(df['y'])
```

![alt text](/images/ch23.png)


 *3. Matplotlip library is imported in order to plot the outcome - Perfect Postive Correlation between columns x and y:*
 
 ```
 %matplotlib inline
import matplotlib.pyplot as plt

```
---

```
plt.scatter(x, y)
plt.show()
```


![alt text](/images/ch24.png)




