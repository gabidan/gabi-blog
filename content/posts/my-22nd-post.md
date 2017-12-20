---
title: "Clustering algorithms"
date: 2017-12-19T21:15:19Z
draft: true
---

### Clustering is an *unsupervised* learning problem where the data is divided into meaningful and/or useful groups. It can be the overall goal of the project or a starting point for an analysis such as data summarization.


---

Types of clustering:


* Exclusive Clustering
* Overlapping Clustering
* Hierarchical Clustering
* Probabilistic Clustering


Examples of clustering algorithms:


* K-means
* Fuzzy C-means
* Hierarchical clustering
* Mixture of Gaussians


An important component of a clustering algorithm is the **distance measure** between data points. 

If the components of the data instance vectors are all in the same physical units then **Euclidean distance** is suitable to successfully group similar data instances. 
However, Euclidean distance can sometimes be misleading. 

Euclidean distance is not a good choice when:

* Data points are measured by differnt units
* The data has many dimensions 


Using clustering algorithms where Euclidean distance is the appropriate measure are:

* Genes data

https://aws.amazon.com/1000genomes/ 

http://pages.cs.wisc.edu/~dpage/kddcup2001/ 

* Geo-groups of social media users (based on the geo-network of their friends)

http://konect.uni-koblenz.de/networks/facebook-wosn-links 


* Text mining (reviews on hotels)

https://github.com/kavgan/opinosis/blob/master/OpinosisDataset1.0_0.zip 

