---
title: 
layout: post
weight: 10
hidden: true
---

===


**Course**: DS   <br/>
**Mod**: Mod 5 Sec 38 V2         <br/>
**Topic**: KMeans Clustering <br/>
**Amount of time**: 60 minutes <br/>
**Author**: Alison Peebles

Adapted from the DS Lesson Starters repository.

***

#### Lesson Summary:

This lesson starts with a conceptual introduction to KMeans, discussing the procedures of the algorithm and some of the subsequent implications including the varied convergence depending on both K and the initial centroid seedings. From there, implementing the KMeans algorithm via scikit-learn is introduced before then discussing methods for evaluating K. The elbox method and the silhoute criteria are then introduced. Afterwards, assumptions for the KMeans algorithm are discussed. Finally, two practice scenarios are given. These provide a good opportunity for further review and direct instruction as well as practice and assessment opportunities to gauge student understanding.

#### Topic:
 
 KMeans clustering

#### Learning goals for this lesson:

- **Assess** what scenarios could use k-means
- **Articulate** the methodology used by k-means
- **Apply** KMeans from sklearn.cluster to a relevant dataset
- **Select** the appropriate number of clusters using k-means and the elbow method
- **Evaluate** the weaknesses and remedies to k-means

#### Prerequisite knowledge:

* Students should have previous experience with pandas DataFrames
* Students should have previous experience with scikit-learn and supervised learning
* 

#### Prequisite Learn-Materials:

* [K-means Clustering](https://github.com/learn-co-curriculum/dsc-k-means-clustering)
* [Market Segmentation with Clustering](https://github.com/learn-co-curriculum/dsc-market-segmentation-clustering)

#### Post Learn-Materials:

* [K-means Clustering - Lab](https://github.com/learn-co-curriculum/dsc-k-means-clustering-lab)
* [Common Problems with Clustering Algorithms](https://github.com/learn-co-curriculum/dsc-common-problems-with-clustering)
* [Market Segmentation with Clustering - Lab](https://github.com/learn-co-curriculum/dsc-market-segmentation-clustering-lab)

Appendix:

* [Hierarchical Agglomerative Clustering](https://github.com/learn-co-curriculum/dsc-hierarchical-agglomerative-clustering)
* [Hierarchical Agglomerative Clustering - Codealong](https://github.com/learn-co-curriculum/dsc-hierarchical-agglomerative-clustering-codealong)

#### Relevant learning goals from Airtable: 

*  CLUSTERING.1.recCm6dsv7YP7l7CG
*  CLUSTERING.1.recIJe43T2hevTBSW
*  CLUSTERING.1.recJbQr8TEE06BF3o
*  CLUSTERING.1.recO44tzcbS9iSnFX
*  CLUSTERING.1.recSMj8pDa8U02sfO
*  CLUSTERING.1.recV0JRGfKCrbBlLp
*  CLUSTERING.1.recVaQmgoFiAjdpu0
*  CLUSTERING.1.recf2fF9igUdUmtKQ
*  CLUSTERING.1.rectFADiERCF8VoIh
*  CLUSTERING.1.recvwR7MprfXRtgsB
*  CLUSTERING.2.rec9phZdBplybJGv8
*  CLUSTERING.2.rec9phZdBplybJGv8
*  CLUSTERING.2.reccQtrtsH8uhVpWa
*  CLUSTERING.2.recjgePLtm4WKmMyY
*  CLUSTERING.2.recl1OLOCwiWoK3OZ
*  CLUSTERING.2.recptvDUSNlc44GO3
*  CLUSTERING.3.recQmS4KE00NxgQHA
*  CLUSTERING.3.recfK3qLOnqN6zTgr
*  CLUSTERING.3.recufCl2Xvghfohe3
*  GRAPH.2.recoHHZESjI8XOAN0
*  GRAPH.2.recrc7qbNQmlnKDwC

#### Materials

* Ipython notebook

#### Vocab / Concepts 

* Clustering
* Centroid
* KMeans
* Inertia
* Elbow Method
* Silhoutte Coefficient

#### Lesson Outline:

* Introducing the KMeans Algorithm
	* Procedure
	* Implications and consequences
		* Varying convergence based on centroid initialization
* Implementing KMeans via scikit-learn
* Choosing K
	* Average distance to cluster center
		* As K > number of points, distance > 0
	* Elbow Method
	* Silhoutte Criteria
* Applied Examples
	* Wine Properties
		* 
	* Online Retail
		* This final example poses some interesting problems for clustering the purchase data; invoice number and customer id are numbers, but strictly identifiers not numerical quantities. As such, any distance calculation based on these fields will be erroneous; customer 12345 and 12346 are not necessarily any more similar than customer 12345 and customer 97531. It may be appropriate to create dummy variables for other categorical fields such as country, but doing so will also create a sparse feature space with many dummy dimensions associated for a single categorical variable which also leads to feature weight imbalances for the KMeans algorithm.