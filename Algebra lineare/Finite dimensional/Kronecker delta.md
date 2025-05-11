---
wiki-publish: true
---
The **Kronecker delta** $\delta_{ij}$ is a function of two discrete variables, typically integer indexes, such that is equal to zero if the indexes are different and to one if they are the same:
$$\delta_{ij}=\begin{cases}
1 & \text{if }i=j \\
0 & \text{if }i\neq j
\end{cases}$$
It commonly arises in linear algebra.
### Usage in nested sums
The Kronecker delta is particularly useful when appearing in nested sums over its indexes. In these cases, one can exploit the nullity in different indexes to make one of the sums vanish, alongside the delta itself. In fact, given some generic values $x_{i}$ and $y_{j}$ dependent on the indexes, we see:
$$\sum_{i=1}^{N} \sum_{j=1}^{N} \delta_{ij}x_{i}y_{j}=\sum_{i=1}^{N}x_{i}y_{i}$$
This is because all terms with $i\neq j$ vanish, leaving only the $i=j$ terms. We can therefore merge the sums and drop the second index.