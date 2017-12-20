---
title: "Chicken weight"
date: 2017-09-23T15:19:34+01:00
draft: true
---


**An experiment was conducted to measure and compare the effectiveness of various feed supplements on the growth rate of chickens**


The data was extracting from the folowing website:

https://vincentarelbundock.github.io/Rdatasets/datasets.html

The following line of code was used to import the data into Pandas and build a data frame:

```
df = pd.read_csv('chickwts.csv')
```


The line of code below presents the first 5 rows of the data frame:

```
df = data.head(5)
```


The outcome is as follows:

>	Unnamed: 0	weight	feed

>0		1		179		horsebean

>1		2		160		horsebean

>2		3		136		horsebean

>3		4		227		horsebean

>4		5		217		horsebean




The line of code below generates the descriptive statistics of the data frame. Analyzes both: numberic and objective series. 

```
df.describe(include = 'all')
```



The outcome is as follows:


>			Unnamed: 0	weight			    feed

>count	 	71.000000	71.000000		    71

>unique		NaN		    NaN					6

>top		NaN		    NaN					soybean

>freq		NaN		    NaN					14

>mean	    36.000000  261.309859			NaN

>std		20.639767   78.073700			NaN

>min		1.000000	108.000000			NaN

>25%		18.500000	204.500000			NaN

>50%		36.000000	258.000000			NaN

>75%		53.500000	323.500000			NaN

>max		71.000000	423.000000			NaN


The descriptive statistics analysis above shows that the data frame countains 71 lines. The minimum weight of the chicken is 108 grams and the maximum weight of the chicken is 423 grams. The middle value of the weight is 261 grams.

There are 6 unique entries describing the type of chicken food, with the most frequent food being the soybeab - it appears in the dataset 14 times. 



**Numerical analysis**

The line of code below produces a graphical representation of the distribution of chicken weights in a form of a histogram:


```
df['weight'].hist()
```


![alt text](/images/ch8.png)


The graph above shows the distribution of the chickens' weight and how many chickens belong to a given weight category.




**Categorical data analysis**

The line of code below groups the data into unique entries, counts how many times each appears in the data set and plots the entry distribution. 

```
df.groupby('feed').count()['weight'].plot(kind='bar')
```


![alt text](/images/ch7.png)

The graph above confirms that the most frequent food appearing in the data set is 'soybean' and it has 14 entries. The least popular food is 'horsebean' and it appears in the data set 10 times. 'Casein', 'linseed' and 'sunflower' appear an equal amount of times: 12.




