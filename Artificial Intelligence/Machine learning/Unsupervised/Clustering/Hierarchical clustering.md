---
wiki-publish: true
---
**Hierarchical clustering** is an iterative form of [[clustering]] that creates cluster by progressively refining existing clusters. There's two types: **agglomerative** hierarchical clustering starts from individual points and merges them to create progressively larger clusters; **divisive** hierarchical clustering starts from the entire dataset and splits it to form progressively smaller ones. The **hierarchy** is the sequence of clusters created during the iterations.

In order for hierarchical clustering to work, we need a way to measure distanced between clusters, not just between individual data points. This *cluster distance* is a function that measures some distance between sets of points (i.e. clusters) instead of two points:
$$d_\text{cluster}:\mathcal{P}^{*}(X)\times \mathcal{P}^{*}(X)\to \mathbb{R}^{+}$$
Some common choices are:
- **Single linkage** (nearest): $d_\text{cluster}(D,D')=\min_{x \in D,x' \in D'}d(x,x')$
- **Complete linkage** (farthest): $d_\text{cluster}(D,D')=\max_{x \in D,x' \in D'}d(x,x')$
- **Average linkage**: $d_\text{cluster}(D,D')=\frac{1}{\lvert D \rvert\lvert D' \rvert} \sum_{x \in D,x' \in D'}d(x,x')$
- **Centroid**: $d_\text{cluster}(D,D')=d(c(D),c(D'))$ where $c(D)\equiv \bar{\mathbf{x}}=\frac{1}{\lvert D \rvert}\sum_{\mathbf{x}\in D}\mathbf{x}$ and $\mathbf{x}$ is the [[centroid]] of $D$.