---
wiki-publish: true
---
The **silhouette index** is a [[performance index]] used in [[clustering]]. For each observation, it considers the average distance to the observations in the *same* clusters and the minimum distanced to observations in *other* clusters. Given a partition $\{ D_{1},\ldots,D_{k} \}\equiv \{ D_{i} \}_{i}$ of a [[dataset]] $D=\bigcup_{i=1}^{k}D_{i}$, it is defined as
$$\bar{s}(\{ D_{i} \}_{i})=\frac{1}{\left\lvert  D  \right\rvert }\sum_{x \in D} \frac{d_\text{other}(x,\{ D_{i} \}_{i})-d_\text{same}(x,\{ D_{i} \}_{i})}{\max(d_\text{other}(x,\{ D_{i} \}_{i}),d_\text{same}(x,\{ D_{i} \}_{i}))}$$
The distance functions are defined as follows:
$$d_\text{other}(x,\{ D_{i} \}_{i})=\min_{x\not\in D_{i}}\min_{x'\in D_{i}}d(x,x'),\qquad d_\text{same}(x,\{ D_{i} \}_{i})=\frac{1}{\lvert x \rvert -1}\sum_{\substack{x,x'\in D_{i} \\ x\neq x'}}d(x,x')$$
The silhouette index is defined between -1 and 1. Higher (closer to 1) is better, as it represents better separated clusters.