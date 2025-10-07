---
wiki-publish: true
---
**Binary classification** is a kind of [[Classifier|classification]] where there are only two possible classes. Typically, these two classes are some variation of "true" and "false". Binary classification is very common, as every "yes or no" question essentially implies a binary classifier. Some examples are: detecting if an email is spam or not, determining whether an image contains a dog or not, or determining if a person is affected by a disease or not.
### Assessment
Assessment is particularly important in binary classification. To illustrate, consider a diagnostic test for a disease $d$. You are told that the accuracy of this test is 99.8%. Is this good or bad? Well, this test is a binary classification problem on
$$X=\{ \text{people} \}\mapsto Y={\{ \text{infected},\text{not infected} \}}$$
If you're told that it gets the diagnosis right 99.8% of the time, that's great!

But say now the diseases is *rare*[^1]. It is known to affect about 2 people every 1000. You are told that the accuracy is again 99.8% percent. Is *this* good or bad? Well, think about this: if you make a "model" that always classifies as "not infected", you'd have an accuracy of 99.8%! This is because over 1000 people, 998 are not infected, so a blind, arbitrarily determined model is incredibly accurate!... obviously this is absurd. The issue here is that we are omitting what "accurate" even means. Or rather, we are omitting what data we are predicting on. This little example contains an important tenet of machine learning:

> Providing accuracy without providing a description of the data is meaningless.

You've seen it here. 99.8% accuracy on a generic disease is great. But the same accuracy on a rare disease is awful and indistinguishable from a dummy classifier. Accuracy alone is not enough information to properly assess a binary classifier. Understanding the data behind the model is mandatory.

So how do we fix the problem? Well, we could look up the accuracy *per class*, meaning how good is the model at predicting each class individually. For instance, our fake test would have a grand 0% accuracy on actually infected people, so that would allow us to determine that the model is actually just snake oil. Providing this kind of additional information is the domain of [[performance index|performance indexes]].

> [!tip] Category convetions
> A common practice in assessment is to assign standard labels to the categories (**positive** and **negative**), then to associate positive with the *rarer* of the two categories. If the rarest does not exist or is not known, then choose arbitrarily which is positive by *clearly stating which is which*. This prevents mix-ups on the scientist or developer side.

Let's try to use the [[False Positive Rate]] and [[False Negative Rate]] performance indexes on this test. The accuracy, we've seen, is
$$\text{Acc}=99.8\%$$
Since it always predicts not-infected (negative), it makes zero mistakes on negatives; there are no false positives.
$$\text{FPR}=\frac{\text{FP}}{\text{N}}=\frac{0}{998}=0\%$$
However, for the same reason, it *never* correctly predicts an infected (positive), meaning all positive cases are actually false negatives:
$$\text{FNR}=\frac{\text{FN}}{\text{P}}=\frac{2}{2}=100\%$$
This shows you at a glance that the model is fundamentally flawed.

In general, always provide both FPR and FNR if you can, alongside accuracy and a description of the data. If you must drop something, start by omitting other indexes, then the accuracy, and only finally the description of the data. You should never drop FPR and FNR unless you have a good reason to (e.g. providing other similar indexes). You should *never* only give accuracy. Also, try to avoid giving only FPR *or* FNR. Provide both in pairs, as just one of the two has more-or-less the same pitfalls as only giving accuracy.



[^1]: What counts as a rare diseases changes from country to country, but that's not important here.
