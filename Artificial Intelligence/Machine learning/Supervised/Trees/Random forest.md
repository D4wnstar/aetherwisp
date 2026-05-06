---
hl-publish: true
---
A **random forest** is an [[ensemble learning]] technique based on [[Decision tree|decision trees]]. It is a stronger form of [[tree bagging]] that improves on individual tree independence.
### Formulation
The basic idea is the same as tree bagging: exploit wisdom of the crowds by creating many trees and aggregating all their predictions. Training many trees and aggregating their answers is easy, but we must also make sure that the trees are independent of each other for wisdom of the crowds to apply. Tree bagging handles independence by randomizing the training sets. Random forests go one step further by *also* randomizing which input features are provided to each tree. This additional form of randomness improves independence and thus effectiveness.

Independent variables (a.k.a. features) are also called **strong predictors**. The idea is the following: if we provide all strong predictors to all trees, they'll probably end up having very similar internal structures since they're all fundamentally doing the same thing. As such, we end up with a bag of many very similar trees. Independence aside, there's a lot of redundancy here. However, if we *omit* some information (i.e. strong predictors) for each tree, we'll force them to predict the result in different ways, thus exploring different aspects of our data and therefore extracting more knowledge from our dataset.

The practical learning technique is relatively simple:
1. Decide the number of trees to train $n_\text{tree}$ and the number of variables to provide to each tree $n_\text{vars}$.
2. For each tree:
	1. Random repetition sample a new training set from the original dataset.
	2. Randomly pick $n_\text{vars}$ variables to retain, deleting all others.
	3. Train the tree.
	4. Add the trained tree to the bag.

When running inference, be careful of providing the correct subset of variables to each tree.
### Complexity
Random forests have two hyperparameters, $n_\text{tree}$ and $n_\text{vars}$. For $n_\text{tree}$, the same conclusions as tree bagging apply. For $n_\text{vars}$, it's fair to ask if it affects complexity. The answer is found empirically: no, it does not. Good default values are $n_\text{vars}=\sqrt{ p }$ for classification and $n_\text{vars}=p/3$ for regression, where $p$ is the number of total variables. Of course, remember to round these to an integer, typically with ceiling rounding.

Since neither hyperparameters affect the tendency to over- or underfit, defaults are usually fine enough (e.g. $n_\text{tree}=500$ and $n_\text{vars}=\sqrt{ p }$ or $n_\text{vars}=p/3$). As such, for practical purposes the random forest can be considered a hyperparameter-free learning technique, as you don't get much value out of optimizing them and you're better off working on other aspects of a [[machine learning system]], like improving the dataset or the UX. These makes random forests rather quick and convenient to work with.