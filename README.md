# Toolbox
Multi-Basin Support-Based Clustering Toolbox for Matlab
(developed by D. Lee, S. Lee, K.-H. Jung, K. Kim, Y. Son, and Jaewook Lee)

The support-based clustering methods, like support vector clustering and Gaussian process clustering, use the contour of an estimated support of a data distribution as a cluster boundary. These methods generally consist in two main steps. First step is support function training step to estimate a support of a data distribution. Second step is cluster labeling step to assign each data to its corresponding cluster. There are many researches focused on the labeling step, for example, complete graph-based strategy, proximity graph-based strategy and dynamic system-based strategy. Also, for the estimation of the support function, in the first step, we can use several algorithms like support vector data description (SVDD) or Gaussian process (GP) The MSCTOOLBOX is the implementation of the support-based clustering method using SVDD and variance of GP as the estimated support function and the basic complete graph-based labeling and a variety of dynamic system-based labeling methods in the Matlab language.


Software Download: please feel free to download the software and refer to the references below. [Multi-Basin Support-Based Clustering Toolbox v1. 0][Link]


References:


S-MSC (Stable Equilibrium Vector)
[1] Jaewook Lee and Daewon Lee, "An improved cluster labeling method for support vector clustering," Pattern Analysis and Machine Intelligence, IEEE Transactions on, vol. 27, pp. 461-464, 2005. [Link]
[2] Hyun-Chul Kim and Jaewook Lee, "Clustering Based on Gaussian Processes," Neural Computation, vol. 19, pp. 3088-3107, 2007. [Link]


T-MSC (Transition Equilibrium Vector)
[3] Jaewook Lee and Daewon Lee, "Dynamic Characterization of Cluster Structures for Robust and Inductive Support Vector Clustering," Pattern Analysis and Machine Intelligence, IEEE Transactions on, vol. 28, pp. 1869-1874, 2006. [Link]
[4] Daewon Lee and Jaewook Lee, "Dynamic Dissimilarity Measure for Support-Based Clustering," Knowledge and Data Engineering, IEEE Transactions on, vol. 22, pp. 900-905, 2010. [Link]


F-MSC (Fast Algorithm)
[5] Kyu-Hwan Jung, Daewon Lee, Jaewook Lee, "Fast support-based clustering method for large-scale problems," Pattern Recognition, vol. 43, pp. 1975-1983, 2010. [Link]

V-MSC (Voronoi Cell Based Labeling)
[6] Kyoungok Kim, Youngdoo Son and JaewoClusteringVoronoi :ll-based Kernel Support Clustering," Knowledge and Data Engineering, IEEE Transactions on, accepted, 2014.

How to use the Multi-Basin Support-Based Clustering Toolbox :

- Create a directory for this toolbox and copy/unzip the toolbox there.
- Go to the toolbox root, ex. (your directory)/msctoolbox.
- Add path for toolbox directory by running 'msctoolbox.m'. Also you can do this by executing 'msctoolbox' at the command prompt.
- Open demo.m file and change some parameters to be appropriate for your problem


Parameters:

| **Parameter**                | **Description**                                              |
| ---------------------------- | ------------------------------------------------------------ |
| **SUPPORT**                  | indicates methods constructing the support functions, which are 'SVDD' and 'GP'. |
| **SUPPORTOPT (for support)** | 'ker' : kerner type. 'rbf' type is desired (for SVDD)  'arg' : argument for kernel and it is different from each kernel (for SVDD)  'C' : regularization constant(default, C=1) (for SVDD)  'hyperparam' : the length scale of autocorrelation, the overall scale of the function, and the amount of noise (for GP) |
| **METHODS**                  | indicates the support vector clustering method, especially its labeling methods. choose among 'CG-SC', 'S-MSC', 'M-MSC', 'T-MSC', 'F-MSC' and 'V-MSC'. |
| **OPTIONS (for methods)**    | 'hierarchical' : use dynamic dissimilarity to do hierarchical clustering  'K' : desired number of clusters when using the hierarchical labeling  epsilon : small value for moving the starting point in finding TPs  'R1' : initial radius of balls in partition phase of the fast support-based clustering  'R2' : intermediate ball merging parameter in the fast support-based clustering |
| **VORONOIOPT**               | 'samplerate' : data sampling rate for estimate support function and labeling  'voronoiMethod' : labeling method for sample data in voronoi cell based clustering  'hierarchical' : Use dynamic dissimilarity to do hierarchical clustering  'K' : desired number of clusters when using the hierarchical labeling  'epsilon' : small value for moving the starting point in finding TPs  'R1' : radius of balls in partition phase of the fast support-based clustering  'R2' : ball merging parameter in the fast support-based clustering  'rho' : fixed constant to compare with the ambiguity ratio for slow phase |
