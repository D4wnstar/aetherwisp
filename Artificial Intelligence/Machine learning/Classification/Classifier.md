---
wiki-publish: true
aliases:
  - classification
---
A **classifier** is a [[machine learning]] [[model]] whose purpose is to classify inputs into a discrete, finite set of labels called **categories** or **classes**. The technique is called **classification**. When given an observation, a classifier tells you what category the observation is a part of.

When there are only two categories, we call the technique [[binary classification]]. If there are more, we call it [[multiclass classification]].
## Types
### Random classifier
The simplest (and least useful) case is **random classifier**, which simply returns a random category. Formally, its prediction function is a [[random variable]]:
$$f_\text{random}=y_{i}\quad\text{where}\quad i\sim U(1,\ldots,\lvert Y \rvert )$$
where $U$ is a [[uniform distribution]] over all possible class indexes. Naturally, this models no dependency between the inputs and outputs: it's just random. In fact, there's no learning phase at all (how could there be?), so it's hard to even call this a model. Nevertheless, it is the theoretically simplest classifier.

There's no real difficulty in building a random classifier: just sample values from a uniform distribution and map them to class labels.
### Dummy classifier
The simplest classifier that is a *proper* model is the **dummy classifier**. Given one specific [[multiset]] of responses $\{ y^{i} \}$, a dummy classifier always predicts the most common class in $\{ y^{i} \}$:
$$f_{\text{dummy},\{ y^{i} \}}=\arg\max\limits_{{y\in Y}} \frac{1}{N}\sum_{i=1}^{N} \mathrm{I}(y=y^{i})$$
where $\mathrm{I}$ is an indicator function that turns "true" into 1 and "false" into 0. We can also package the sum and indicator into a function $\text{Fr}$ of its own:
$$f_{\text{dummy},\{ y^{i} \}}=\arg\max\limits_{y\in Y}\text{Fr}(y,\{ y^{i} \})$$
This is the first real model, because in order to determine what the most common class is, the model must be trained on the set of responses. It provides better-than-random accuracy simply on behalf of the fact that the most common class is, well, the most common, so if you have to pick randomly, always choosing the most common option is your best bet. However, this still models no dependency between $x$ and $y$.
#### Building
To build a dummy classifier, consider the learning process as a [[supervised machine learning]] technique. The two steps are:
1. In the *learning phase*, compute the frequency or [[probability]] of classes.
2. In the *prediction phase*, choose the most frequent class.

Formally, the process of building a dummy classifier is
1. Determine the parameterization of the model. There's quite a few equivalent option:
	1. The model is an array of the class probabilities, $\mathbf{f}=(f_{1},\ldots,f_{\lvert Y \rvert})$. The model space is $M=F_{Y}=\{ \mathbf{f}\in[0,1]^{\lvert Y \rvert}\ |\ \lVert \mathbf{f} \rVert_{1} = 1\}$. It's a [[vector space]] where each vector component is between 0 and 1 and each vector is [[Normalization|normalized]] according to the one-[[norm]] (i.e. the sum of all components, $\lVert \mathbf{x} \rVert_{1}=\sum_{i}x_{i}$).
	2. The model is a [[probability mass function]] $p$ over $Y$. The model space is $M=P_{Y}=\left\{  p\ |\ Y\mapsto[0,1]\text{ such that Prob}(y'=y)=\sum_{y'\in Y}p(y')=1  \right\}$. It's the set of all possible PMFs over categories.
	3. The model is the $y$ part of a [[dataset]] $\{ (x^{i},y^{i}) \}$. The model space is $M=\mathcal{P}^{*}(Y)$.
	4. The model is the most frequent class $y^{*}$. The model space is $M=Y$.
2. The template function to be made is $f_\text{learn}':\mathcal{P}(X\times Y)\mapsto M$.
3. The learning function to be made is $f'_\text{predict}:X\times M\mapsto Y$.
## Assessment
The responses of a classifier are drawn from a finite, discrete [[set]] of classes. We define the **classification error (rate)** on the pairs of predicted and real responses $\{ y^{i},\hat{y}^{i} \}_{i=1,\ldots,N}$ as
$$f_\text{err}(\{ y^{i},\hat{y}^{i} \}_{i=1,\ldots,N})=\frac{1}{N}\sum_{i=1}^{N} \mathrm{I}(y^{i}\neq \hat{y}^{i})$$
where $N$ is the number of test examples and
$$\mathrm{I}=\begin{cases}
1 & \text{if true} \\
0 & \text{if false}
\end{cases}$$
is an indicator function that turns boolean values into numbers. This function returns a number between 0 and 1, with 1 being a 100% error rate and 0 being a perfect outcome. Alternatively, the **classification accuracy (rate)** $f_\text{acc}$ has the same definition of the error, but with $y^{i}=\hat{y}^{i}$ instead. The two are related by
$$f_\text{acc}=1-f_\text{err}$$
We want the accuracy to be as close to 100% as possible. This is unlike in statistics, where we accept that there must some sort of intrinsic variance in the phenomenon that makes 100% unrealistic.
### Bounds
While theoretically between 0 and 1, accuracy receives stricter bounds from the nature of the classifier. The two extreme cases are
1. The model $m$ perfectly models the real world $s$; the accuracy is 1.
2. The model $m$ is completely random; the accuracy depends on the type of classifier.
	1. For a random classifier, considering all possible [[multiset|multisets]] of responses $\mathcal{P}^{*}(Y)$, the accuracy is (on average!) $1/\lvert Y \rvert$.
	2. For a dummy classifier, the accuracy is $\max\limits_{y\in Y}\text{Fr}(y,\{ y^{i} \})$. It is dependent on the training set of responses $\{ y^{i} \}$.