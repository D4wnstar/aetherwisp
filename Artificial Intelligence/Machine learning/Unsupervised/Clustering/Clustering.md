---
hl-publish: true
---
**Clustering**, in the context of [[unsupervised machine learning]], refers to techniques that detect **clusters** or **groups** of data within the [[dataset]]. A cluster, intuitively, is a collection of data points that are close together. Their definition therefore hinges on the concept of "distance" in the space of data points.

Formally, clustering is the process of partitioning a [[multiset|bag]] in sub-bags that contain points that are close together. Given a bag $D\in P^{*}(X)$ representing a dataset of samples from the space $X$, clustering means to find a partitioning $\{ D_{1},\ldots,D_{k} \}$ of $D$ such that the elements of each sub-bag $D_{i}$ are close together according to some distance metric. The choice of distance metric, threshold of "close together" and number of clusters $k$ are open choices that depend on the individual clustering technique and input dataset.

Clustering can be explained as a biobjective [[optimization problem]]:
$$\begin{align}
\max\limits_{D_{1},\ldots,D_{k}}&\left( \sum_{i\neq i'}\sum_{\substack{x \in D_{i} \\ x' \in D_{i'}}}d(x,x') \right)-\left( \sum_{i}\sum_{x,x'\in D_{i}}d(x,x') \right) \\
\text{subject to}&\quad D_{1}\cup\ldots\cup D_{k}=D\quad\text{and}\quad D_{i}\cap D_{i'}=\emptyset \quad \forall i,i'\in \{ 1,\ldots,k \}
\end{align}$$
In simpler terms, we
- maximize distance between points in different clusters (first sum)
- minimize distance between points in the same cluster (second sum)
- require that the clusters form a partition (conditions)

For any $k$ and $d$, there exists one optimal solution. The problem is finding it, as simply enumerating all possible partitions is not feasible due to the combinatorial explosion of possible cases. Unsupervised clustering techniques use ML to "bypass" the enumeration phase to approximate the solution far more efficiently.
## Assessment
Assessing a clustering model can be done through [[performance index|performance indexes]]. Typically, these measure the separateness or density of clustering. Some examples are the [[silhouette index]] and the [[Dunn index]].