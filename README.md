# K-means++ Algorithm
Drawback of standard K-means algorithm:

One disadvantage of the K-means algorithm is that it is sensitive to the initialization of the centroids or the mean points. So, if a centroid is initialized to be a “far-off” point, it might just end up with no points associated with it, and at the same time, more than one cluster might end up linked with a single centroid. Similarly, more than one centroid might be initialized into the same cluster resulting in poor clustering. For example, consider the images shown below. 

A poor initialization of centroids resulted in poor clustering.  

K-mean++:

To overcome the above-mentioned drawback we use K-means++. This algorithm ensures a smarter initialization of the centroids and improves the quality of the clustering. Apart from initialization, the rest of the algorithm is the same as the standard K-means algorithm. That is K-means++ is the standard K-means algorithm coupled with a smarter initialization of the centroids.

nitialization algorithm:

The steps involved are: 
 
Randomly select the first centroid from the data points.
For each data point compute its distance from the nearest, previously chosen centroid.
Select the next centroid from the data points such that the probability of choosing a point as centroid is directly proportional to its distance from the nearest, previously chosen centroid. (i.e. the point having maximum distance from the nearest centroid is most likely to be selected next as a centroid)
Repeat steps 2 and 3 until k centroids have been sampled
