---
wiki-publish: true
aliases:
  - flexibility
  - complexity
---
A **model**, in the context of [[machine learning]], is a set of machine-chosen parameters that complete a hand-made [[template]] function that can then be used to infer predictions. The combination of a model $m$ and its template $f'(x,m)$ provides a prediction function $f_\text{predict}(x)=f'(x,m)$. When using template-based learning, the template is chosen by hand, so finding a model for it becomes the end goal of the machine learning process.

A model is obtained by running a template-based learning technique on a [[Dataset|learning set]]. The model is said to be **learned**, **trained** or **fitted** on the dataset. Formally, the model is one output of the learning technique, as an element $m$ of the space of all possible sets of parameters $M$. Informally, the term is also often used to refer to a still-untrained set of parameters (e.g. "train a model")[^1].
### Complexity
Models usually have a large number of parameters or a large number of steps in its template procedure. Both of these aspects contribute to the **complexity** of the model. Complexity is a property of each individual model, not of the learning technique, so models trained with the same technique can have wildly different complexities based on the training set and parameters. Pretty much every learning technique has at least one parameter that affects the maximum complexity of the created models; this parameter is sometimes called **flexibility** and it represents a sort of "permitted complexity." Broadly speaking, flexibility should be chosen based on how difficult the problem is to solve (in practice, the dataset). Too much flexibility in simple problems leads to over-engineered solutions that are either inefficient, don't generalize or both; in statistical terms, **overfitting**. Too little flexibility in difficult problems leads to poor results because the models does not have the tools to solve such a complex problem; in statistical terms, **underfitting**. Tuning flexibility also helps greatly in overcoming noise in the data, which you want to not fit since it does not carry any information.

When talking about complexity, underfitting is often referred to having **high bias**. This is because underfitting leads to the models that tend to generate decisions that are biased toward some $y$ values. Mathematically, underfitting weakens the correlation between inputs $x$ and outputs $y$. In the extreme case of complete underfitting, we get a model that takes decisions that are entirely unrelated to the input.

Similarly, overfitting is also referred to as **high variance**. This is because if you repeat the learning process on the *same dataset*, you can get wildly different models that take very different decisions. This is not good because there is one and only one real world process that generated the data[^2] and a proper training run should converge to that process. If the model changes each time, then this suggests that the model is not actually converging to any real world system and "inventing" a new explanation every time.

Flexibility should be chosen based on metrics that measure over- or underfitting in order to find an optimal value in the middle.

[^1]: Learning techniques also don't have a well-defined end, so determining what counts or doesn't count as an output is a fool's errand. Does one step of training on some random initial parameters count as making a model? The convenient answer is "who cares; all sets of parameters are models, but some models are better than others."

[^2]: Obviously there could be more processes at play, but the *sum* of these processes is unique. The model only "sees" the sum of the processes because that's the information that the data contains. For instance, if you're trying to predict the height of a person based on their age, there are an enormous amount of biochemical processes that lead to that result, but the model doesn't care, because it's not predicting any of those in particular. It's the predicting the collective effect of all of them.
