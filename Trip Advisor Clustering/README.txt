@@@@Data Mining using clustering @@@

# Background
This project aims at practicing data mining using clustering and classification algoritgms. I used the Titanic data set which has been used on Kaggle (https://www.kaggle.com/broaniki/titanic) as the basis for classification method to analyze the relationship between the predictors and passengers¡¯ survival probability, and how to choose the most significant ones to build the model. When it comes to clustering part, I used Trip Advisor Reviews data set which is from (https:// archive.ics.uci.edu/ml/datasets/Travel+Reviews), which is a web site hosted at the University of California at Irvine (UCI) that contains a large number of data sets which people use for testing data mining methods. I used multiple clustering methods in this part to category the 10 attributes for the clustering model.

#Important Note:

Moving forward, this part involves which questions have been answered during the modeling process for the two different data sets.

# What to read for Tripadvisor:
Note: the steps I conducted below involve data cleaning, building the model, estimation and plotting...

6.Data overview ** 
I used data.describe() to take a look of the data. There are 980 instances in the whole data set. And there is no missing values in every attributes which is a good start.
Then I did the plot for every attributes¡¯ distribution. Here I load the library of seaborn as sns and matplotlib.pyplot as plt

7.K-means clustering ** 
In this case, I put K into the list which is 3,5,10. There are 980 instances in the whole data set. And there is no missing values in every attributes which is a good start. The results of overall clustering score and silhouette coefficient and the Calinski score, also the clustering 2D plot. I used the code below to load the libraries I need for the process.

# from sklearn import metrics
#from sklearn.metrics import calinski_harabaz_score
#from sklearn.cluster import KMeans


8.Agglomerative clustering ** 
A In order to do the comparison, K here is also should be one of 3,5,10. This algorithm is different from K-means method. It doesn¡¯t have overall score to do estimation. However, it still involves many other ways including the 2D plot to test the performance. I used the code below to load the libraries I need for the process.

# from sklearn import cluster
# clst1=cluster.AgglomerativeClustering(n_clusters=3)
#clst1.fit(data_cluster)

9.DBSCAN clustering ** 
The difference between the two above and DBSCAN is DBSCAN doesn¡¯t need to set the clustering numbers. In this algorithm, eps and min_sample are two important parameters in the model. When eps goes up, the number of categories will be larger. When mini_sample goes down, the number of categories will be bigger. In order to do the comparison, K here is also should be one of 3,5,10. So in this case, I set the parameters specifically so that the clustering numbers would be the same with another two algorithms. I used the code below to load the libraries I need for the process.

# from sklearn.cluster import DBSCAN
#from sklearn.preprocessing import StandardScaler
#X = StandardScaler().fit_transform(data_cluster)
#dbs1 = DBSCAN(eps = 0.1, min_samples =3).fit(X)#from sklearn.metrics import roc_curve, auc


