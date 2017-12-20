---
title: "The Netflix shows"
date: 2017-09-27T21:10:49+01:00
draft: true
---

![alt text](/images/netflix.png)


### A data set which explores rating distributions of Netflix shows

The csv data file was imported into Pandas in order to create a data frame from a website listed below:

https://inclass.kaggle.com/chasewillden/netflix-shows

```
data = pd.read_csv('netflix.csv', encoding = "ISO-8859-1")
```

After exploring the first 5 lines of the data frame:

```
data.head()
```

![alt text](/images/ch12.png)


A new data frame consiting of 2 colums was created in order to explore the patterns of the user ratings:

```
data1=data[['title', 'user rating score']]
```

![alt text](/images/ch13.png)



---



**Numerical analysis**

To begin with, user scoring is clustered, and it is explored how many shows fall into each rating category:

```
data1.hist()
```

![alt text](/images/ch14.png)


*The graph above shows that the largest propotion of shows fall into a rating category of 95 and above, which is a really encouraging score. It suggests that Netflix users have been largely satisfied with Netflix content*


---


**Categorical analysis**

Firstly, it is explored what is the highest user score, which show(s) received it and how many users have given that score:

```
data1.max()
```



```
data1[data['user rating score']==99].groupby('title').count().plot(kind='bar')
```

![alt text](/images/ch15.png)

*The graph above shows that the show scored highest by Netflix users is: '13 Reasons Why' and 8 Netflix users have given this show the highest score*



