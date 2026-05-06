---
hl-publish: true
---
A **decision tree** is formal description and visualization of a sequence of decisions. It is also a kind of [[supervised machine learning]] [[model]]. A decision tree is a graph of nodes, where each node is either a decision, after which the tree ends, or a further question, which are followed by at least two more nodes. Decision nodes are called **leaves** and question nodes are called **branches**. If branch nodes split in exactly two, the structure is also known as a **binary tree**. In computer science terms, decision trees are a sequence of neste `if-else` statements.

Decision trees are generally used for [[classification]]. Leaf nodes return a category, whereas branch nodes contain conditions on the independent variables used in order to choose between categories. The tree is turned into a model which spontaneously determines the branches based on learning examples. Formally, a decision takes some $\mathbf{x}\in X$ input variable and return some category $y$ out of an unordered [[set]] $Y$. The tree is an object $t\in T_{p,Y}$ that maps $X$ to $Y$ where each leaf is a category $y\in Y$ and each branch is a pair $(j,\tau)$. Here, $j\in \{ 1,\ldots,p \}$ is the index of the independent variable we are testing in the branch and $\tau$ is the threshold for decision. For instance, if $\mathbf{x}\in \mathbb{R}^{N}$, then we could have a branch $(2,120)$ that could represent the condition $x_{2}\geq 120$.
## Binary trees
### Notation
A binary decision tree $t\in T_{L}$ is represented as
$$t\equiv[l;t';t'']$$
where $L$ is the space of all **labels**, $l$ is the label of this tree, $t',t''\in T_{L}\cup \emptyset$ are the left and right children trees. Essentially, we treat a tree as a nested collection of nodes with a label that split into a left and right tree. Each child tree $t',t''$ have the same structure here. Leaf nodes have no children and are therefore always $t_\text{leaf}=[l;\emptyset,\emptyset]\equiv[l]$. A **label** $l$ is either a category $l\in Y$ (for leaves) or an index-threshold pair $(j,\tau)$ as described above (for branches).

> [!example]- Age and height
> Say you need to determine who's allowed on a carnival ride. You only allowed kids 10 years old and older and 120 cm tall or taller. The tree has two branches: $(1,10)$ and $(2,120)$, where $x_{1}\equiv x_\text{age}$ and $x_{2}\equiv x_\text{height}$. The input domain is $X=X_\text{age}\times X_\text{height}$ and $Y=\{ \text{allowed},\text{not allowed} \}$. We can write this tree compactly as
> $$t=[(1,10);[\text{not allowed}];[(2,120); [\text{not allowed}]; [\text{allowed}]]]$$
### Template
The template prediction function $f'_\text{predict}$ of a binary decision tree is a recursive function that takes an input $\mathbf{x}$ and a tree $t$ and returns a category $y$. It's essentially an `if-else` that either exists with a category (on a leaf node) or calls the left or right tree (on a branch).
### Learning
Training a binary tree follows the human logic for choosing how to make the decision threshold. In short, there's only two steps:
1. Put a vertical or horizontal line in the input domain that splits the data in a good way.
2. Repeat step 1 for each two of the splits.

This runs until we are satisfied with the results. This process, the $f'_\text{learn}$ function, is called **recursive binary splitting**. It's a recursive function that takes a [[dataset]], splits the data in two parts, starting from the whole dataset[^1], and creates a node with the most frequent class when stopping recursion.

```
pseudocode here
```

(Finish this: 21/10/25)

The dummy classifier version of `find_best_branch` is fine but we can do better. Instead of using the error, there's a couple more metrics we can use to determine how to splits: the **[[Gini index]]** and the **[[cross entropy]]**. In both cases, the lower is better, but it is found empirically that the Gini index works better for decision trees in particular, so unless you have a particular need, that's the one you should use. These two metrics measure **node impurity**, which is the amount of cases that are different from the most common one (i.e. the dummy classifier) from the examples that arrive at a certain node[^2]. Essentially, "for all the examples that get to this node, how many are wrongly classified by the dummy classifier?"

We can also improve the stopping condition. The simple case we started with is based off of data size. This stops when we run out of data ($n\leq n_\text{min}$) or the data that we do have has no errors, meaning it's all correctly classified ($\text{Err}(D)=0$). One alternative is **tree depth** $\tau_{d}$, so the number of splits in the tree. In this case, we stop when the tree goes deeper than $\tau_{d}$ splits or when there are no errors. Another option is **node impurity**, where we stop when the impurity is beneath a certain threshold. Large tree depths or low node impurities make, in general, bigger trees.
#### Probabilistic learning
We can further refine the probability distribution by making the tree return a [[probability mass function]] instead of a guaranteed category. Basically, the tree learns to determine how likely its prediction is instead of giving you a sure answer. Instead of deciding "this is the category", it decides "there is an 80% chance this is the category and a 20% it's this other."

In probabilistic learning, the learning function has the same domain, but the prediction function now returns a PMF instead, so we redefine it as $f''_\text{predict}:X\times M\to P_{Y}$, where $P_{Y}$ is the space of all possible PMFs over the categories. Given an observation $\mathbf{x}\in X$ and a tree model $t\in M$, it returns a PMF $p\in P_{Y}$.

```
pseudocode here
```

### Explainability
The simplicity of the decision tree models gives them the unique of advantage of being very *transparent*, meaning it's easy to explain what the tree is doing and how it's taking its decisions. This is because trees are just `if-else` chains, so inspecting a tree is just inspecting a series of `if-else` thresholds. Besides being of [[explainable AI|scientific interest]], this can be of enormous importance in domains where responsibility is high, such as medical or legal decision making. Knowing what the model is doing greatly increases our trust and confidence in it because we can tell what it's doing right and what its weaknesses are.
### Complexity
The [[Artificial Intelligence/Machine learning/Model|complexity]] of a binary tree is determined by a the $n_\text{min}$ parameter, which is its flexibility parameter. The lower $n_\text{min}$ is, the more complex the tree is allowed to be. When $n_\text{min}\to +\infty$, no complexity is permitted and the binary tree collapses to a dummy classifier. Overly low $n_\text{min}$ lead to overfitted trees and overly large $n_\text{min}$ values lead to underfitted ones.

Trees unfortunately suffer from rather poor flexibility, in the sense that they are rather prone to either over- or underfitting, meaning that they are not great at modeling complex datasets. However, since they are cheap to train, one sensible pattern to follow to improve their flexibility is to train *several* trees with high complexity (which will all probably overfit) and then choose the *common* parts of their output as the actual model. The fine details of each tree will likely be unwanted noise, but it's pretty much guaranteed that they will all fit the same general shape: this common shape contains a lot of information about the system, but is guarded against noise by dropping out the specifics of each individual tree. This method is an application of **wisdom of the crowds**, a concept that says that the opinion of many is almost always more valuable than the opinion of one.

Wisdom of the crowds is not infallible. It only really works if:
1. we have many opinions (otherwise you'd be better off finding, very well thought-out opinion)
2. they are all independent (otherwise they'd basically just be one big repeated opinion)
3. we have a way to aggregate them (we still need *one* answer in the end)

In trees, this opinions and people translate to predictions and trees. In other words, we need many trees, all independently trained, and an aggregate to combine their predictions. Training many trees is not a problem, so point 1 is easy. Finding aggregates is also not hard. In classification, the aggregate is the majority category; in regression, it's some average metric (e.g. mean, median, mode...)[^3]. So we're only missing point 2: how do we guarantee independence?

Assuming the learning technique is deterministic (it is, in general, for trees), training $n$ trees on the *same* dataset $D_\text{learn}$ using the same (hyper)parameters will give us $n$ *identical* models. As such, they are completely *not* independent. Therefore, this cannot work. We need to change something every training run. So what then? In practice, we split the dataset in $n$ smaller pieces and train trees on those. One option is to (sort of) do [[cross-validation]] by shuffling the training set, splitting in $n$ folds and then train $n$ trees. The issue is that unless our datasets is massive, any significant value of $n$ will make each training set tiny and each tree won't have enough data. A better option is to instead start from the entire dataset for each tree, but do random sampling to make up new training sets. The trick to make better use of our data is to allow repetitions, meaning you can have multiple of the same pair in same dataset. Then, each training set $D_{\text{learn},i}$ is $\lvert D_\text{learn} \rvert$ randomly-sampled pairs from $D_\text{learn}$, which can be repeated. As such, each training set has the same size as the original set, managed by padding with repetitions. Due to randomness, each training set is *mostly* independent of each other and retains the same size, at the cost of poorer data. This learning technique ($n$ decision trees with random repetition sampling) is called **tree bagging** and is a form of [[ensemble learning]].

The model returned by tree bagging is a bag of trees. It contains $n_\text{tree}$ trees, which is a tunable hyperparameter of the technique. Uniqueness is not guaranteed: the bag can contain two identical trees (but probably won't, since training is not deterministic). Training a bag of trees amounts to applying random repetition sampling on the dataset to make $n_\text{tree}$ different variants of it, then training one tree per variant. Each tree is individually trained with a low $n_\text{min}$ value (usually $n_\text{min}=1$) to intentionally let the tree overfit and gather a lot of information on its dataset. Inference is then a two step process: first, calculate a prediction for each individual tree in the bag; second, aggregate all the predictions into a final one with the appropriate technique (majority, mean, etc.).

What's the flexibility of tree bagging? We arbitrarily set $n_\text{min}$ of each tree to be the same and for the method to work, we need a small value, so that's out of the question. Instead, we have $n_\text{tree}$ to work with. How does changing this affect flexibility? Well, the question is a bit complicated to answer. On one hand, increasing the number of trees *surely* increases flexibility because there's just more parameters in total. On the other, aggregation of the final answer prevents the increase of trees from having a significant effect of the final answer due to smoothing. In practice, the answer is given empirically: tree bagging is more effective than an individual tree for sufficiently large $n_\text{tree}$ and notably, high $n_\text{tree}$ does not lead to overfitting. What "sufficiently large" means depends on the system, but it usually refers to tens or hundreds of trees[^4].

[^1]: This top-down approach is called **divide-et-impera**.

[^2]: Actually, error does too, but these two metrics do it better.

[^3]: Actually, with sets of regression trees you're basically working with a statistical set. Mean, mode, etc. are central statistics, but you can also calculate dispersion statistics like [[Variance]] to measure the *uncertainty* of the prediction.

[^4]: Of course, be careful of your resources! Training more trees is naturally more expensive, so consider if the added cost is worth the improvement.
