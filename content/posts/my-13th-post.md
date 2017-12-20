---
title: "5000 IMDB movies"
date: 2017-10-02T17:44:39+01:00
draft: true
---

The csv data file was downloaded from the website below:

https://www.kaggle.com/suchitgupta60/imdb-data 

A data frame was created and the first 5 lines of the data were explored using the following lines of code:

```
data = pd.read_csv('tmdb.csv')
```

```
data.head()
```

The first insights are aimed at the genre of the movies, therefore, the structure of the 'genre' column was explored:

```
data['genres'].head()
```


![alt text](/images/ch16.png)


```
data['genres'].apply (lambda x : type(x))
```


![alt text](/images/ch17.png)
	


