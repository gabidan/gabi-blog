---
title: "Starting with R"
date: 2017-10-02T21:36:29+01:00
draft: true
---

![alt text](/images/rpro.jpg)

#### R is an open source programming language and software environment for statistical computing and graphics. 
The R language is widely used among statisticians and data miners for developing statistical software and data analysis.

---

R can be downloaded from the following website:

http://cran.ma.imperial.ac.uk/ 



The following steps are taken to import and explore a CSV data file:


*1. Ensure you are in the correct directory by checking what files are stored in your current path. Use the function below:*


```
dir()
```


*2. Change the directory to where your CSV file is stored:*
	
	
![alt text](/images/chdir.png)


*3. Create a data frame using the following line of code (in this case, the data frame is called nflx):*

```
nflx<-read.csv("netflixdata.csv")
```





*4. Explore the summary of the data frame:*

```
str(nflx)
```


![alt text](/images/rdatafr.png)


*The outcome above suggests that our data frame has 1000 lines and 7 columns. The titles of the colums listed on the left include names such as: 'title', 'rating', ratingLevel' etc.* 


*5. Use the following lin eof code to explore the first 10 lines of the data frame:*

```
head(nflx, n=10)
```







		
