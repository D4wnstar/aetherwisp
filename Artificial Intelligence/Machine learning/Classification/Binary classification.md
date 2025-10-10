---
wiki-publish: true
---
**Binary classification** is a kind of [[Classification|classification]] where there are only two possible classes. Typically, these two classes are some variation of "true" and "false". Binary classification is very common, as every "yes or no" question essentially implies a binary classifier. Some examples are: detecting if an email is spam or not, determining whether an image contains a dog or not, or determining if a person is affected by a disease or not.
### Assessment
Assessment is particularly important in binary classification. To illustrate, consider a diagnostic test for a disease $d$. You are told that the accuracy of this test is 99.8%. Is this good or bad? Well, this test is a binary classification problem on
$$X=\{ \text{people} \}\mapsto Y={\{ \text{infected},\text{not infected} \}}$$
If you're told that it gets the diagnosis right 99.8% of the time, that's great!

But say now the diseases is *rare*[^1]. It is known to affect about 2 people every 1000. You are told that the accuracy is again 99.8% percent. Is *this* good or bad? Well, think about this: if you make a "model" that always classifies as "not infected", you'd have an accuracy of 99.8%! This is because over 1000 people, 998 are not infected, so a blind, arbitrarily determined model is incredibly accurate!... obviously this is absurd. The issue here is that we are omitting what "accurate" even means. Or rather, we are omitting what data we are predicting on. This little example contains an important tenet of machine learning:

> Providing accuracy without providing a description of the data is misleading.

You've seen it here. 99.8% accuracy on a generic disease is great. But the same accuracy on a rare disease is awful and indistinguishable from a dummy classifier. Accuracy alone is not enough information to properly assess a binary classifier. Understanding the data behind the model is mandatory.

So how do we fix the problem? Well, we could look up the accuracy *per class*, meaning how good is the model at predicting each class individually. For instance, our fake test would have a grand 0% accuracy on actually infected people, so that would allow us to determine that the model is actually just snake oil. Providing this kind of additional information is the domain of [[performance index|performance indexes]].

> [!tip] Category conventions
> A common practice in assessment is to assign standard labels to the categories (**positive** and **negative**), then to associate positive with the *rarer* of the two categories. If the rarest does not exist or is not known, then choose arbitrarily which is positive by *clearly stating which is which*. This prevents mix-ups on the scientist or developer side.

Let's try to use the [[False Positive Rate]] and [[False Negative Rate]] performance indexes on this test. The accuracy, we've seen, is
$$\text{Acc}=99.8\%$$
Since it always predicts not-infected (negative), it makes zero mistakes on negatives; there are no false positives.
$$\text{FPR}=\frac{\text{FP}}{\text{N}}=\frac{0}{998}=0\%$$
However, for the same reason, it *never* correctly predicts an infected (positive), meaning all positive cases are actually false negatives:
$$\text{FNR}=\frac{\text{FN}}{\text{P}}=\frac{2}{2}=100\%$$
This shows you at a glance that the model is fundamentally flawed.

In general, always provide both FPR and FNR if you can, alongside accuracy and a description of the data. If you must drop something, start by omitting other indexes, then the accuracy, and only finally the description of the data. You should never drop FPR and FNR unless you have a good reason to (e.g. providing other similar indexes). You should *never* only give accuracy. Also, try to avoid giving only FPR *or* FNR. Provide both in pairs, as just one of the two has more-or-less the same pitfalls as only giving accuracy.

Alright, say you *do* have both FPR and FNR, and you have two models you have assessed. How do you choose which of the two is better? Say the two models are $m_{1}$ and $m_{2}$, and they performance indexes are
$$\text{FPR}_{1}=6\%,\quad\text{FNR}_{1}=4\%,\qquad\text{FPR}_{2}=10\%,\quad\text{FNR}=1\%$$
Which is better? Well... we don't really know as is. We need more information: the *cost of the error*. Making an error is assumed to come with a cost[^2], and realistically a false positive and false negative have different costs. So, at a broad level, the quality of a model is a weighed average of the FPR and FNR, with the cost of error being the weights:
$$c=c_\text{FP}\text{ FPR N}+c_\text{FN}\text{ FNR P}$$
where $\text{P}$ and $\text{N}$ are the total observations. What the cost of the error is is entirely *domain knowledge* and problem dependent. A spam filter will have different costs from a diagnostic test on a life-threatening disease. For example, having a false positive on a spam filter has little cost (it's easy to open your spam folder and find the email that was falsely flagged), but a false negative might be dangerous (someone might get scammed because an email didn't get caught).

Once you have cost metrics, we can optimize for lowest cost. Given a model, we can tune it to prefer avoiding FPs over FNs (or viceversa). For example, in a disease test, you probably want to avoid FNs, as even if someone gets falsely flagged, it's less dangerous than accidentally missing the disease. Formally, we can build an intermediate prediction function $f''_\text{predict}$ defined as
$$\begin{align}
f''_\text{predict}:X\times M&\mapsto P_{Y} \\
f''_\text{predict}(x,m)&=p
\end{align}$$
It takes the observation and the model as input and gives you a [[Probability distribution]]. This probability then needs to be turned into a decision, which we can simply do by taking the decision with the highest probability (the "best"). Formally:
$$f'_\text{predict}(x,m)=\arg\max\limits_{y\in Y}(f''_\text{predict}(x,m))(y)\tag{1}$$
This kind of method is called a **supervised learning technique with probability** (for classification). It is defined by
1. an $f'_\text{learn}:\mathcal{P}^{*}(X\times Y)\mapsto M$ for training a model from a dataset;
2. an $f''_\text{predict}:X\times M\mapsto P_{Y}$ for giving a probability distribution to take decisions from.

$f'_\text{predict}$ is then known in advance: it's $(1)$. As usual, $f_\text{predict}(x)=f'_\text{predict}(x,m)$ given a known $m$. In the definition of $f''_\text{predict}$, $P_{Y}$ is the space of all possible probability distributions on the set of categories. In binary classification, the only possibility is
$$p(y)=\begin{cases}
p_\text{pos} & \text{if }y=\text{pos} \\
p_\text{neg}=1-p_\text{pos} & \text{if }y=\text{neg}
\end{cases}$$
with $p_\text{pos}\in[0,1]$. In the binary case specifically, you could add a third function
$$\begin{align}
f'''_\text{predict}:X\times M&\mapsto[0,1] \\
f'''_\text{predict}(x,m)&\mapsto p_\text{pos}
\end{align}$$
and use this instead of $f''_\text{predict}$ (well, it's a specific case of it). The closer $p_\text{pos}$ is to 0.5, the less confident the model is (since 50% is random chance). We can define the **confidence** as
$$\text{conf}(x,m)=\frac{\lvert p_\text{pos}-0.5 \rvert}{0.5}=\frac{\lvert f'''_\text{predict}(x,m)-0.5 \rvert}{0.5} $$
It's defined in $[0,1]$ and you want it to be as high as possible.

This is assuming 0.5 is the **threshold** between positive and negative. We can turn this threshold into a parameter $\tau$ and change it to bend how likely positive and negative predictions are. A lower $\tau$ will make positives more likely and viceversa. Mathematically:
$$f^{\tau}_\text{predict}(x,\tau)=\begin{cases}
\text{pos} & \text{if }f'''_\text{predict}(x,m)\geq \tau \\
\text{neg} & \text{otherwise}
\end{cases}$$
0.5 should be considered the default, but it can be varied if you want to make the model more or less sensitive to positives or negatives.

Given the same model $m$ and the same input-output pairs $\{ (\mathbf{x}^{i},y^{i}) \}$, we can state that
1. the greater $\tau$ is, the less frequent positive responses are, leading to lower FPR and greater FNR
2. the lower $\tau$ is, the more frequent positive responses are, leading to higher FPR and lower FNR.

Note that the greater-or-equal is important: if we slam $\tau$ to zero, then it's impossible to predict negatives, so FNR naturally goes to zero (can't get negatives wrong if you never bet on negative!), but if you slam $\tau$ to one, then FPR does *not* go to zero. This is because even with $\tau=1$, it's technically possible to predict a positive when $f'''_\text{predict}=1$ exactly (due to the equal), so while FNR goes lower, it does not go down to zero.

Using this $\tau$ parameter, we can define the **Equal Error Rate** (**EER**), which is the value of FPR and FNR when the two match at a specific $\tau=\tau _\text{EER}$. It's a sort-of performance metric: you want it to be as low as possible. It's formally defined in $[0,1]$, but in practice you'll find it in $[0,0.5]$.

You could also visualize this parameter in a different way: given a sequence of values $\tau_{1},\ldots,\tau_{M}$, we can make a **receiving operating characteristic curve** (**ROC curve**). It is a plot of TPR vs. FPR for different values of $\tau$. A perfect classifier will stay at the top left corner, where $\text{TPR}=1$ and $\text{FPR}=0$. It's common to draw a dashed line from the bottom left to the top left; this represents a random classifier, those are the values that a random classifier will give for a variable $\tau$. A healthy classifier should always be on the left of this line (if it isn't, it's somehow worse than a random classifier, which shouldn't possible...).

While the ROC curve itself isn't an index, we can get one by calculating the **area under the curve** (**AUC**). Since TPR and FNR are normalized, AUC is also in $[0,1]$. In practice, it's $[0.5,1]$ because 0.5 is the random classifier's AUC and realistically you shouldn't be able to go that low. A perfect classifier has $\text{AUC}=1$.

Alright, let's back up a minute. We've been talking about variable $\tau$ for a few paragraphs, but we've never talked about how to pick a reasonable set of $\tau$ values, say for calculating EER or AUC. There's a few options:
- evenly spaced values between $[0,1]$ at $n+1$ points.
- evenly spaced values in a subinterval $[\tau _\text{min},\tau _\text{max}]$. Same as before, but leaves out extreme values which realistically won't be used in practice.
	- a trick to choose the subinterval extremes are to look at the lowest and highest $f'''_\text{predict}$ values in the dataset and choose $\tau _\text{min}$ and $\tau _\text{max}$ to be these extremes. No point in choosing an interval larger than the model will predict.
- midpoints of $\{ p_\text{pos}^{i} \}_{i}$, where $p_\text{pos}^{i}=f'''_\text{predict}(x^{i},m)$. This is interesting because it guarantees that each $\tau_{i}$ will be between two responses, meaning each $\tau_{i}$ will give a different response (as opposed to the previous two ways, which might give $\tau_{i}$ close enough that there's no difference between the two). This is the most informative way and should be the default choice.

Let's put this all together:
- If you know the cost of errors, pick a $\tau$ that you think is appropriate, then calculate FPR and FNR and finally the cost $c$.
- If you don't know the cost of error, but you do know which $\tau$ to use, then measure FPR and FNR at $\tau=0.5$, then calculate EEC.
- Finally, if you don't know either, measure FPR and FNR at $\tau=0.5$, then calculate AUC.

Finally, if you can, it's best to calculate everything: more information for proper assessment never hurt anyone.

One last thing on binary classification assessment: given a [[multiset]] $\{ (y^{i},\hat{y}^{i}) \}_{i}$ of pairs, we define an object called the **confusion matrix**, which is a [[matrix]] which has
- one row for each value of $y\in Y$ (*true* labels)
- one column for each value of $\hat{y}\in Y$ (*predicted* labels)
- one entry for each pair, containing the number of cases where $\hat{y}^{i}=\hat{y}$ and $y^{i}=y$.

You can use the confusion matrix to find accuracy, TPR and TNR by doing some matrix operations.

[^1]: What counts as a rare diseases changes from country to country, but that's not important here.

[^2]: No point is doing all this effort to make an ML model if making mistakes has no cost. At that point just roll a die.
