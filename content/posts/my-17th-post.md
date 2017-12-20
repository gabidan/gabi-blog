---
title: "R Language - the basics"
date: 2017-10-08T20:15:45+01:00
draft: true
---


### Math and Variables

The image belows shows the basic commands of variable assignemt and mathematical operations:

![alt text](/images/ch18.png)


### Matrix

A matrix is created using the function **matrix**. **It is ordered by colums by default.** 

```
x = matrix(data=c(1,2,3,4), nrow=2, ncol=2)
```
nrow and ncol can be omitted:

```
x = matrix (c(1,2,3,4),2,2)
```


![alt text](/images/ch19.png)


A matrix can be created using intervals:

```
x = matrix(1:16, 4, 4)
```

An element can be selected from the matrix:

![alt text](/images/ch20.png)

Or multiple and and columns can be selected:

![alt text](/images/ch21.png)
