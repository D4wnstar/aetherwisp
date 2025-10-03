---
wiki-publish: true
aliases:
  - learning set
  - training set
  - test set
---
A **dataset**, in the context of [[machine learning]], is a collection of data used as training or evaluation material for an [[AI model]]. The shape and content of a dataset varies widely depending on the learning technique, scope, purpose and architecture of the model and available resources. Datasets are commonly called **learning** or **training sets** when used for the learning phase and **test sets** when used for the assessment phase.

The word "set" can be a bit misleading because datasets are not traditional mathematical [[set|sets]]. This is because they may contain duplicates, which is disallowed by definition in sets. A set that allows duplicates is known as a **[[multiset]]** (or **bag**). Datasets are therefore multisets (or bags) of data.
### Supervised learning
In [[supervised machine learning]], the dataset is composed of *pairs* of inputs and outputs:
$$D_\text{super}\equiv \{ (\mathbf{x}^{i},\mathbf{y}^{i}) \}_{i=1,\ldots,N}$$
where $\mathbf{x}^{i}$ is an input, $\mathbf{y}^{i}$ is an output and $N$ is the total number of examples pairs (the [[cardinality]] of the set, $N=\lvert D \rvert$). Indexes are written as superscript since inputs and outputs are usually [[Vector space|vectors]] and this notation avoids conflict with component indexes.

In supervised learning sets, the dataset must be consistent with the domain $X$ and codomain $Y$ of the prediction function $f_\text{predict}:X\mapsto Y$ to be learned. Formally, $D_\text{super}$ is an element of a space $\mathcal{P}^{*}(X\times Y)$, where
- $X\times Y$ is the [[Cartesian product]] of the input and output spaces;
- $\mathcal{P}(X\times Y)$ is the [[power set]] of $X\times Y$;
- $\mathcal{P}^{*}(X\times Y)$ is the power set *with duplicates* of $X\times Y$ (a "multipowerset" if you prefer). It is the set of all possible multisets of $X\times Y$.

A dataset can be seen as a [[matrix]] where each row is a input-output pair and each column is a component of the pair. For example, a dataset of $M$ pairs, where $\mathbf{x}^{i}\in \mathbb{R}^{N}$ and $y^{i}$ is any one-dimensional variable, can be written as
$$D=\begin{pmatrix}
x_{1}^{1} & \ldots & x_{j}^{1} & \ldots & x_{N}^{1} & y^{1} \\
\vdots &  & \vdots  &  & \vdots  & \vdots \\
x_{1}^{i} & \ldots & x_{j}^{i} & \ldots & x_{N}^{i} & y^{i} \\
\vdots &  & \vdots &  & \vdots  & \vdots \\
x_{1}^{M} & \ldots & x_{j}^{M} & \ldots & x_{N}^{M} & y^{M}
\end{pmatrix}$$
Some common nomenclature about this matrix is
- Each row $x_{1}^{i},\ldots,x_{N}^{i}$ is an **observation**.
- Each column $x_{j}^{1},\ldots,x_{j}^{M}$ is a **feature**.
- Each cell $x_{j}^{i}$ is the **value** of the $i$-th observation for the $j$-th feature.
- Each $y^{i}$ is a **response**. If $y^{i}$ is a [[categorical variable]], it's also called a **class label**.

Here $N$ is the number of independent variables $x_{1},\ldots,x_{N}$ and $M$ is the number of pairs in the dataset. Other common letters are $p$ for the variables and $n$ for the pairs. On the assumption that the dataset describes the whole problem, these quantities then define the "size" of the problem.
### Unsupervised learning
In [[unsupervised machine learning]], the dataset is just a bag of inputs:
$$D_\text{unsuper}\equiv \{ \mathbf{x}^{i} \}_{i=1,\ldots,N}$$

[^1]: Despite this, in practice the data is often processed in sequential order. This is more of a property of the learning technique than the dataset though.
