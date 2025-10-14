---
wiki-publish: true
aliases:
  - learning set
  - training set
  - test set
---
A **dataset**, in the context of [[machine learning]], is a collection of data used as training or evaluation material for a [[model]]. The shape and content of a dataset varies widely depending on the learning technique, scope, purpose and architecture of the model and available resources. Datasets are commonly called **learning** or **training sets** when used for the learning phase and **test sets** when used for the assessment phase.

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
### Balancing
The distribution of the data inside the dataset is important in [[classification]]. A dataset is said to be **balanced** with respect to the response variable if the frequency of each category in the dataset is roughly the same. In [[binary classification]] specifically, this means that the dataset about half positive and half negative cases. This means that $\text{P}\simeq\text{N}$. We can make some considerations on the inherent accuracy of the dataset by expressing error rate through [[False Positive Rate|FPR]] and [[False Negative Rate|FNR]]:
$$\text{Err}=\frac{\text{FP}+\text{FN}}{\text{N}+\text{P}}=\frac{\text{P}\cdot\text{FNR}+\text{N}\cdot\text{FPR}}{\text{N}+\text{P}}\simeq \frac{\text{N}(\text{FNR}+\text{FPR})}{\text{2N}}=\frac{1}{2}(\text{FNR}+\text{FPR})$$
On a balanced dataset, the error rate is the average of FPR and FNR. The accuracy is
$$\text{Acc}=1-\text{Err}\simeq\frac{1}{2}(\text{TNR}+\text{TPR})\tag{1}$$
The more unbalanced the dataset is, the further the accuracy or error diverges from this mean, making the model progressively more *misleading* if the only metric that is provided is error or accuracy. This is why FPR and FNR should be provided alongside the accuracy.

In [[multiclass classification]], the definition of balancing gets more complicate. In general, in unbalanced dataset it's common to use **weighted accuracy** (or **balanced accuracy**). It is defined as
$$\text{wAcc}=f_\text{wAcc}(\{ (y^{i},\hat{y}^{i}) \}_{i})=\frac{1}{\lvert Y \rvert }\sum_{y\in Y}\left( \frac{\sum_{i}\mathrm{I}(y^{i}=y\text{ and }y^{i}=\hat{y}^{i})}{\sum_{i}\mathrm{I}(y^{i}=y)} \right)=\frac{1}{\lvert Y \rvert }\sum_{y\in Y}\text{Acc}_{y}$$
It's the unweighted average of the accuracy of each class. It's called weighed because it ignores the exact amount of data points for each class, unlike usual accuracy. It is therefore resilient even in unbalanced datasets. As usual, the greater the better. This is the multiclass equivalent of $(1)$.
### Learning data, testing data
Datasets aren't just used for training. Assessing the quality of a model is a necessary part of a machine learning pipeline and the assessment process also relies on data. A model is considered to work well if it predicts the same outcomes as the real world process it's modeling. In order to run test predictions, we need test data, and we also need some testing function $f_\text{effectiveness}$ that measures how effective the model is[^2]. This function takes the learning technique and a dataset as input, and returns a numerical output representing the model's effectiveness. Formally
$$\begin{align}
f_\text{effectiveness}:\mathcal{L}_{X\mapsto Y}\times \mathcal{P}^{*}(X\times Y)&\mapsto \mathbb{R} \\
f_\text{effectiveness}(f'_\text{predict},m,D)&\mapsto E
\end{align}$$
where $E$ is the effectiveness. Essentially, it trains a model on the dataset using the learning technique, then tests it, and finally returns the model's effectiveness. This function requires *training the entire model* every time it's used! Be mindful of this in the rest of this section.

There are arguments to be made regarding how to pick this test data. In principle, we could use the same dataset that we used to train the model, $D_\text{learn}$. But in practice, that's a bad idea. This is because this does not test the model's ability to *generalize*. Generalization is the model's ability to perform well on data that it did not see during its training, so-called **unseen data**. Testing on the training set will almost always give greatly exaggerated performance values.

Realistically, test data should *never* be present in the training set[^3]. The data you have access to should be split in two parts: the training set $D_\text{learn}$ and the test set $D_\text{test}$. The ratio of data split between the two is up to you, but a common split is 70% training data, 30% test data. If you are short on training data, you can remove some test data to turn it into training data, but not too much. This process does measure generalization ability because the test data is unseen and is the standard way of doing model testing. It does however have a flaw: since the split is static, meaning it's decided once and never changed, it leads to this process having *robustness* issues. That means that the training/test data split might be "unlucky"; for example, if you're training a [[Binary classification|binary classifier]] and have an unbalanced dataset, you could end up with all positives in the train set and all negatives in the test set. The model will then not learn any negatives and the model will be a mess. Thus, care should be taken on how the data is split.

To improve robustness, we can instead run the test multiple times on *randomized* test sets. The randomization occurs $k$ times and the test is ran that many times, returning $k$ effectiveness values. The [[mean]] of these values is then taken. This is a more robust method, because it guarantees that the "unlucky data" factor is largely negligible, because the chance of getting $k$ unlucky datasets is minuscule. What you lose with this procedure is performance: you now have to run the test $k$ times, which might be difficult or unrealistic if the model is expensive to train.

A common technique is called **cross-fold validation** (**CV**). It is like repeated randomized tests, but it guarantees that each test set is disjoint from every other, meaning each iteration of the test uses entirely different data. Each test subset is called a **fold**. Each fold contains $1/k$ of the total data. This method improves the significance of each individual iteration, since it guarantees that each test is completely different from the previous ones.

An specific form of CV is **leave-one-out CV** (**LOOCV**). It is simply a CV where the number of folds $k$ is equal to the number of data points $\lvert D \rvert$. Each fold then is just a single data point. Essentially, you run a test on a single piece of information for every single piece of information the model trained on, then average all the results. This is obviously *extremely* expensive computationally speaking, so it's only efficient for models that are very cheap and fast to train and/or have little data available.

Now, repeated random, CV and LOOCV all provide a [[sample]] of effectiveness results. We spoke of the mean before, but we can also compute other statistical properties, namely [[standard deviation]]. Where mean tells you how effective the model is on average, the standard deviation tells you how consistent the learning technique is on different datasets[^4]. Once you start to see these values as statistical data, you can start to use all the tools of statistics to analyze how the model performs: for instance, you can draw a [[boxplot]], run a [[hypothesis test]], or more.
#### Hypothesis tests
Hypothesis tests (or statistical significance tests) have an entire discipline of statistics revolving around. This section is a brief primer on them specifically for use in machine learning assessment.

A statistical significance test is a procedure that, given two samples $\{ x_{A,i} \}_{i}$ and $\{ x_{B,i} \}_{i}$ of two [[Random variable|random variables]] $X_{A}$ and $X_{B}$ and a set of hypotheses $H_{0}$ (called the null hypothesis), it returns a number $p \in[0,1]$, called the $p$-value. This value represents the [[probability]] that, by collecting other samples from the same random variables and *assuming that $H_{0}$ still holds*, the two new samples are more unlikely than the original two.

Let's make an example. Our samples are $\{ 1,1,2,2,3,3 \}$ for $X_{A}$ and $\{ 0,0,1,0,1,1 \}$ for $X_{B}$. Our hypotheses $H_{0}$ are
1. $X_{A}$ is [[Gaussian distribution|normally-distributed]].
2. $X_{B}$ is normally-distributed.
3. The means are identical, $\mu_{A}=\text{E}[X_{A}]=\mu_{B}=\text{E}[X_{B}]$.

If we run the test and get $p=0.90$, that means
1. If you resample $X_{A}$ and $X_{B}$, you are very likely to find samples that are less likely than the ones we started with, as long as $H_{0}$ holds.
2. Thus, our samples are very likely (since others are almost certainly less so).
3. Thus, I can assume that $H_{0}$ is probably true.

If we instead get $p=0.01$, that means
1. As before, but you are very *un*likely to find less likely samples.
2. Thus, our samples are very *un*likely (since others are almost certainly more so).
3. Thus, I can assume that $H_{0}$ is probably false.
	- It's still possible that you got very unlucky with your samples and they returned a false negative. But it's unlikely.

In practice, there are many concrete significance test one can use. Two common ones are the **[[Wilcoxon test]]** and the **[[Friedman test]]** (and all their variations). What you do with them is pick one based on the $H_{0}$ you have (these often revolve around stating that $\mu_{A}>\mu_{B}$ or $\mu_{A}\neq \mu_{B}$), apply them to calculate $p$, then hope it's as low as possible. You then compare it to an arbitrary threshold $\alpha$ and hope that $p<\alpha$. If that's true, then the test is statistically significant.

For more, see [[Hypothesis test]] and [[Estimator#Confidence intervals]].

[^1]: Despite this, in practice the data is often processed in sequential order. This is more of a property of the learning technique than the dataset though.

[^2]: By "effective" we mean how good its predictions are. A perfectly effective model performs exactly like the real world.

[^3]: If the training set contains test data, that's commonly called **contamination** and it generally makes that test's results fake and exaggerated.

[^4]: In fact, we can do these for all [[performance index|performance indexes]] of the models trained during the tests. For instance, the mean and standard deviation of the [[Binary classification|AUC]].
