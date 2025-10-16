---
wiki-publish: true
aliases:
  - classifier
  - dummy classifier
  - random classifier
  - perfect classifier
  - Bayes classifier
---
**Classification** is a [[machine learning]] technique that produces a [[Artificial Intelligence/Machine learning/Model|model]], called a **classifier**, whose purpose is to classify inputs into a discrete, finite set of labels called **categories** or **classes**. When given an observation, a classifier tells you what category the observation is a part of.

When there are only two categories, we call the technique [[binary classification]]. If there are more, we call it [[multiclass classification]].
## Types
### Random classifier
The simplest (and least useful) case is **random classifier**, which simply returns a random category. Formally, its prediction function is a [[random variable]]:
$$f_\text{random}=y_{i}\quad\text{where}\quad i\sim U(1,\ldots,\lvert Y \rvert )$$
where $U$ is a [[uniform distribution]] over all possible class indexes. Naturally, this models no dependency between the inputs and outputs: it's just random. In fact, there's no learning phase at all (how could there be?), so it's hard to even call this a model. Nevertheless, it is the theoretically simplest classifier. A fair coin toss is a random binary classifier. A fair $N$-faced die is a random $N$-multiclass classifier.

There's no real difficulty in building a random classifier: just sample values from a uniform distribution and map them to class labels.
### Dummy classifier
The simplest classifier that is a *proper* model is the **dummy classifier**. Given one specific [[multiset]] of responses $\{ y^{i} \}$, a dummy classifier always predicts the most common class in $\{ y^{i} \}$:
$$f_{\text{dummy},\{ y^{i} \}}=\arg\max\limits_{{y\in Y}} \frac{1}{N}\sum_{i=1}^{N} \mathrm{I}(y=y^{i})$$
where $\mathrm{I}$ is an indicator function that turns "true" into 1 and "false" into 0. We can also package the sum and indicator into a function $\text{Fr}$ of its own:
$$f_{\text{dummy},\{ y^{i} \}}=\arg\max\limits_{y\in Y}\text{Fr}(y,\{ y^{i} \})$$
This is the first real model, because in order to determine what the most common class is, the model must be trained on the set of responses. It provides better-than-random accuracy simply on behalf of the fact that the most common class is, well, the most common, so if you have to pick randomly, always choosing the most common option is your best bet. However, this still models no dependency between $x$ and $y$.
#### Building
To build a dummy classifier, consider the learning process as a [[supervised machine learning]] technique. The two steps are:
1. In the *learning phase*, compute the frequency or [[Probability]] of classes.
2. In the *prediction phase*, choose the most frequent class.

Formally, the process of building a dummy classifier is
1. Determine the parameterization of the model. There's quite a few equivalent option:
	1. The model is an array of the class probabilities, $\mathbf{f}=(f_{1},\ldots,f_{\lvert Y \rvert})$. The model space is $M=F_{Y}=\{ \mathbf{f}\in[0,1]^{\lvert Y \rvert}\ |\ \lVert \mathbf{f} \rVert_{1} = 1\}$. It's a [[vector space]] where each vector component is between 0 and 1 and each vector is [[Normalization|normalized]] according to the one-[[norm]] (i.e. the sum of all components, $\lVert \mathbf{x} \rVert_{1}=\sum_{i}x_{i}$).
	2. The model is a [[Probability mass function]] $p$ over $Y$. The model space is $M=P_{Y}=\left\{  p\ |\ Y\mapsto[0,1]\text{ such that Prob}(y'=y)=\sum_{y'\in Y}p(y')=1  \right\}$. It's the set of all possible PMFs over categories.
	3. The model is the $y$ part of a [[dataset]] $\{ (x^{i},y^{i}) \}$. The model space is $M=\mathcal{P}^{*}(Y)$.
	4. The model is the most frequent class $y^{*}$. The model space is $M=Y$.
2. The template function to be made is $f_\text{learn}':\mathcal{P}(X\times Y)\mapsto M$.
3. The learning function to be made is $f'_\text{predict}:X\times M\mapsto Y$.
### Perfect classifier
A **perfect classifier** is the upper bound of classifier accuracy. It is simply defined as a classifier that always provides a correct classification, meaning that it works precisely like the real-world phenomenon $s$:
$$f_\text{perfect}(x)=s(x)$$
Of course, just like the random classifier it's largely a theoretical object, but it acts as the best case scenario for classification. Realistically, a perfect classifier is only possible in a deterministic system. Stochastic systems have inherent [[random|randomness]] that makes them impossible to predict perfectly.
### Bayes classifier
Under the assumption of a stochastic system, what's the best possible classification we can make? The **Bayes classifier** is an ideal model of a real stochastic system. It is defined as
$$f_\text{Bayes}(x)=\arg\max\limits_{y\in Y}\text{Prob}(s(x)=y\ |\ x)$$
The function $\text{Prob}(s(x)=y\ |\ x)$ is the probability that, given $x$, the real system $s$ will return $y$. This classifier essentially always predicts the most likely case for every possible category, using the real system $s$ as its guide.

It can be proven that the Bayes classifier is the best (i.e. most accurate) classifier on a given [[multiset]] of observations $\mathcal{P}^{*}(X)$. Its accuracy is $\leq100\%$. Like the dummy classifier, it is a proper model since it requires observations from the real world. However, creating a Bayes classifier requires known $s$, which is unreasonable in practice[^1]. Given the direct presence of probability, it's intuitive to notice that the more random the system is, the poorer the Bayes classifier will be (and thus the upper bound of accuracy for all realistic models).
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
While theoretically between 0 and 1, accuracy receives stricter bounds from the nature of the classifier. More realistically, the bounds on all possible data are given by the theoretical bounding classifier types. By "all data" we mean all the theoretically possible datasets for $y$, meaning the [[power set]] $\mathcal{P}^{*}(Y)$. If we only have access to a set of responses $\{ y^{i} \}_{i}$ the bounds are
1. For a random classifier, considering all possible [[multiset|multisets]] of responses $\mathcal{P}^{*}(Y)$, the accuracy is (on average!) $1/\lvert Y \rvert$.
2. For a perfect classifier, the accuracy is $100\%$.

If we also have access to a set of observations $\{ x^{i} \}_{i}$ we can improve the bounds to
1. For a dummy classifier, the accuracy is $\max\limits_{y\in Y}\text{Fr}(y,\{ y^{i} \}_{i})$. It is dependent on the training set of responses $\{ y^{i} \}$.
2. For a Bayes classifier, the accuracy is $\leq 100\%$. It gets lower the more random the process being predicted is.

|                                  | Lower bound                                           | Upper bound |
| -------------------------------- | ----------------------------------------------------- | ----------- |
| By definition                    | 0                                                     | 1           |
| All data                         | $1/\lvert Y \rvert$                                   | 1           |
| All data, with one set of inputs | $\max\limits_{y\in Y}\text{Fr}(y,\{ s(x^{i}) \}_{i})$ | $\leq 1$    |

To elaborate on "all data": of course in the world we won't encounter every possible combination of data. Some sets of data are more likely than others. For instance, if you're building an email spam filter, your inputs $x$ will be strings, so $X$ is the space of all possible strings. But it's pretty obvious that some strings will be more likely than others; "Good day" is more likely to be found than "nduasipncq". This information is actually *very* valuable because it further refines our error bounds. If we know (or more likely approximate) the natural distribution of the data we're working on (call them $f_{i}$, one for each class), then the approximate lower bound of the random classifier becomes $\max\limits_{i}f_{i}$. This is better than the uniformly-distributed $1/\lvert Y \rvert$ we originally guessed. The more imbalanced the natural distribution is, the better the bare-minimum accuracy!

To conclude, in a realistic system where we have a proper collection of observations $\{ x^{i} \}_{i}$ (these observations are **representative** of the real world), the actual range of accuracy that one should expect is
$$[\max\limits_{y\in Y}\text{Fr}(y, \{ s(x^{i}) \}_{i}),\ 1-\epsilon]$$
where $\epsilon>0$ is an intrinsic uncertainty due to the stochastic nature of the phenomenon.

[^1]: And even if it were, if you know $s$ already why are you even building a classifier to approximate it?
