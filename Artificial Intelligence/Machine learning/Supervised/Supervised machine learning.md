---
wiki-publish: true
---
**Supervised machine learning** is a branch of [[machine learning]] that studies learning techniques based on a [[dataset]] of examples, meaning pairs of observations and responses. The machine learns how to connect the two by inferring relationships from the examples.
## Formalism
A supervised learning technique is a way for learning a prediction function $f_\text{predict}\in \mathcal{F}_{X\mapsto Y}$ from a dataset of examples $D\in \mathcal{P}^{*}(X\times Y)$, each being a pair of an input $x \in X$ and an output $y\in Y$. This process is done by a higher-order function $f_\text{learn}$ that takes the dataset as an argument and returns the prediction function:
$$\begin{align}
f_\text{learn}:\mathcal{P}^{*}(X\times Y)&\mapsto\mathcal{F}_{X\mapsto Y} \\
D&\mapsto f_\text{predict}=f_\text{learn}(D)
\end{align}$$
The learning technique is the learning function $f_\text{learn}$.

Supervised learning techniques can be interpreted as an optimization problem: given a dataset $D$, find the $f_\text{predict}$ that describes it the most optimal way. As such, it is in principle possible to apply classical optimization methods to a supervised machine learning problem. While true, in practice this is complicated greatly due to the dimensionality of the spaces. $X$ and $Y$ can be very high-dimensional on their own (e.g. $\mathbb{R}^{N}$ with high $N$), so $X\times Y$ becomes massive very fast, not to mention $\mathcal{F}_{X\mapsto Y}$ being an infinite-dimensional function space. From a computational perspective, running classical optimization on these spaces is borderline impossible.

The dimensionality problem can be made better by artificially considering $f_\text{predict}$ to take a certain form. By "form" I mean the "kind" of function it is. If $X,Y$ are real numbers, you could assume $f_\text{predict}$ to be a linear function, which reduces the function space to $\mathcal{F}_{X\mapsto Y}=\{ f\ |\ f=ax+b\text{ with }a,b\in \mathbb{R} \}$. If $X$ is textual (e.g. UTF-8 strings) and $Y$ is Boolean, you could assume $f_\text{predict}$ is a regular expression, which reduces the function space to the set of possible regular expressions. In any case, this provides very valuable information about the problem.

We can use this information to make a **[[template]]**. A template is a function that is mostly defined by hand, but contains undefined pieces that are left to the machine learning process to figure out on its own. Basically, it's the best of both worlds: we define the parts that we understand (or at least want) by hand and only leave the things we don't understand for the machine to learn. The template is some function in the reduced function space: $f'\in \mathcal{F}'_{X\mapsto Y}$. In the previous linear function example, the template would be the generic linear function $f'(x)=ax+b$ with $a,b\in \mathbb{R}$. We have fixed the shape by hand and the model now only needs to find $a$ and $b$.[^5]

A template becomes a prediction function once you apply the set of parameters it asks for. If we call $m\in M$ a specific set of parameters in the space of all possible ones we can say
$$f_\text{predict}(x)=f'_\text{predict}(x,m)$$
In the linear case, $m=\{ a,b \}$ and $M\equiv \mathbb{R}^{2}$. The set of parameters $m$ is called a **[[model]]**. Once you have a model, you can slot it in the template and you can start making predictions using it. If it does not provide the results you want, you can retrain a different model using different parameters and reuse the same template.

Recall that $f'\in \mathcal{F'}_{X\mapsto Y}$, but we have defined $f'$ as $f'\equiv f'(x,m)$. $x$ is an observation, we don't control what it is; we do however control the model $m$. Thus, when training on a template, $f_\text{learn}$ does technically explore $\mathcal{F}'_{X\mapsto Y}$ to return a specific form of $f'$, but in practice the only thing we actually care about is $m$ because we already know the general $f'$. Thus, we can instead talk about an $f'_\text{learn}$ that takes a dataset as an input and returns a model:
$$\begin{align}
f'_\text{learn}:\mathcal{P}^{*}(X\times Y)&\mapsto M \\
D&\mapsto m=f'_\text{learn}(D)
\end{align}$$
Then, since we know the general $f'_\text{predict}$ template, we just give it $m$ to get $f_\text{predict}$. In this case, the learning technique is the pair of model learning function and prediction template, $(f'_\text{learn},f'_\text{predict})$. It's an equivalent definition to the previous one, but more useful in practice. Unless otherwise stated, the rest of this article refers to this definition.

> [!success] Summary
> A supervised learning technique is a way of finding a prediction function from a dataset of examples $D$. There's two equivalent ways to formalize it:
> 1. The technique is a function that takes a dataset and returns a prediction function: $f_\text{learn}(D)=f_\text{predict}$.
> 2. The technique is a function that takes a dataset and returns a model designed to work on a hand-made template: $f'_\text{learn}(D)=m$ and $f'_\text{predict}(x,m)=f_\text{predict}$.
### Categories
Supervised learning techniques are a very broad topic and differ in many ways. Some important aspects are
- applicability: what must $X$ and $Y$ be and they applicable to the problem at hand? For instance, a technique might require $X\equiv \mathbb{R}^{N}$ and $Y\equiv \mathbb{R}$.
- efficiency: how much data does the technique need to return a good outcome? How fast does it run?
- effectiveness: how good is the resulting $f_\text{predict}$?
- interpretability and explainability:  do we understand why or how the technique does what it does? Do we understand its outcome?

Because of the massive breadth of options, there exist conventional categories to organize specific kinds of techniques. These categories are defined on the basis of what kind of $X,Y$ and $M$ the techniques work with. Below are some types.

With respect to $Y$:
- If $Y$ is a finite set without intrinsic order, the technique is called **classification** and the model is a **[[classifier]]**. The elements of $Y$ are called **categories** and $y\in Y$ is said to be a **categorical variable**. If there are only two possible categories ($\lvert Y \rvert=2$), then we have **[[binary classification]]**. If there are more, we have **[[multiclass classification]]**.
- If $Y$ is the set of real numbers $\mathbb{R}$ (or a subset), the technique is called **regression**. $y\in Y$ is said to be a **numerical variable**.

With respect to $X$:
- If $X=X_{1}\times\ldots\times X_{N}$ where each $X_{i}$ is either $\mathbb{R}$ or a finite set of, we say that $\mathbf{x}\in X$ is a **$N$-tuple** and the technique is **multivariate**. Each $x_{i}$ component of $\mathbf{x}$ may be categorical or numerical and is an **independent variable**. Meanwhile, $y\in Y$ is a **dependent variable** of $\mathbf{x}$. Some names of $\mathbf{x}$ are **feature**, **attribute** or **predictor**.
- If $X$ is the set of all strings, the technique is called **text mining**.
## Assessment
Once a model is built using supervised learning, we need to assess whether it does what we want it to. There's three things we can assess: the entire [[machine learning system]], the model used by the system or the training technique used.

Given some axis $a$ representing some metric of judgement, we can either assess *absolutely* (does the model have a perform well in terms of $a$ according to some end purpose?) or *comparatively* (does the model perform better than other models in its class?). When talking about absolute assessment, it's useful to analyze all three components: is the system good enough? Is the model good enough? Is the technique good enough?[^1] When dealing with comparisons, comparing models is the most obvious things, but the learning technique is also important; a great model trained with a horrendously inefficient technique might not be justifiable compared to a slightly-worse-but-still-good model trained with a technique that's 10x more efficient. If the outcome of the model is some quantity (say a number, rating, etc.), this number can also be evaluated for correctness. Is it within a certain range? How often is it correct?

Ideally, our assessment should return a number. Numbers are easy to remember, write, compare and process. They make it easy to do both kinds of assessments above. In principle, we want this number to be a direct representation of the real-world **effectiveness** of the model, meaning its ability to make good decisions in realistic situations for its use case. A test of effectiveness is usually called a **benchmark**.

Measuring the effectiveness is not easy. In fact, it gets harder the more complicated the ML system. This measurements rests on the assumption that there exists some real correlation about the inputs and outputs. For instance, there is a correlation between height and your likelihood of becoming a top basketball player, but there is no correlation between the color of the chair you're sitting on and the likelihood of you becoming a rock star. However, you *can* make models for both and you'll get some prediction function in both cases. But the predictions in the latter case will never make any sense: the correlation is inherently lacking and any detected correlation is just chance. To assess effectiveness is to admit that such a real correlation exists and that the model is picking up on it. If it it doesn't exist, there's no point in testing in the first place as the model in fundamentally flawed. Mathematically, $y\propto x$ and there exists some **real system** $s:X\mapsto Y$ that maps $x$ to $y$. The model then tries to "reverse engineer" $s$ based on observed examples; its attempt is $f_\text{predict}$. Some other times it might the opposite: the real system is the inverse $s^{-1}:Y\mapsto X$ and our model is predicting the inverse process[^2]. Either way, both are valid.

Assessment then boils down to comparing how closely $f_\text{predict}$ matches $s$ (how closely the ML system matches the real world). In theory, there's two paths we can take to compare them.
1. A **direct comparison** means "opening up" $f_\text{predict}$ and $s$ and comparing their internals, hoping that they are quite similar.
2. An **indirect comparison** means comparing the *behavior* of $f_\text{predict}$ and $s$ and seeing if they match. We do this by feeding the model with some examples we know that behavior of and seeing if $f_\text{predict}$ returns similar results to $s$.

In practice, however, direct comparison are nearly impossible most of the time. Much of the world is far too complex to get an analytical description of it, and most of the time, the same is true of the model too. But more importantly, a direct comparison implies having access to $s$. But if we have $s$, meaning an analytical description of the real phenomenon, then *we don't need ML*. Just use $s$! You already have the answer, no need to reinvent the wheel. In practice, you're only ever going to use indirect comparisons.

To run indirect comparison, we'll need to make some function $f_\text{IC}:\mathcal{F}_{X\mapsto Y}\times \mathcal{F}_{X\mapsto Y}\mapsto \mathbb{R}$ that takes two predictors (real world $s$ + ML system $f_\text{predict}$) and returns some number[^3]. This is your assessment value. What this value is comes down to choice. Often it's some percentage of correct answers or an ELO ranking like in chess. Either way, it's a number that you can compare between different tests on different models and that can be simplified down to $[0,1]$. At a high level, the pseudocode of your assessment procedure is something along these lines:

```
function assess_model(f_predict, s) {
	test_inputs = get_test_set()
	real_responses = s(test_inputs)
	model_responses = f_predict(test_inputs)
	assessment = compare_responses(real_responses, model_responses)
	return assessment
}
```

There's two new functions in here: $f_\text{get test set}$ and $f_\text{compare responses}$. The former is essentially a placeholder for the test dataset. The latter is how good the comparison methodology is. The latter is important, but the former is critical! Well made test data is arguably the single most important part of testing. Wrong, imprecise or unrealistic test examples or a training dataset contaminated with the test set can completely invalidate an entire benchmark regardless of every other factor. Quality of the test data comes down to many factors, but two important ones are *data size*, the number of tests, and *data coverage*, how varied the tests are. Both these contribute to how *representative* the tests are of the real world. More tests and more coverage both mean better representation[^4], but coverage is nicer to optimize because it does not increase the amount of tests, meaning you spend less time (and money) running tests.

As for the comparison function, we can formally define the signature as $f_\text{compare responses}:\mathcal{P}^{*}(Y^{2})\mapsto \mathbb{R}$ where each element $(y,\hat{y})\in Y^{2}$ is a pair of responses from the model and the real world. Note that it's only dependent on the responses; the inputs do not matter at all. The outcome of the comparison is called a **[[performance index]]**.

To go into greater detail on assessment, we need to determine what *kind* of model we're testing.
### Classification
If the model is a [[classifier]], its responses are drawn from a finite, discrete [[set]] of classes. We define the **classification error (rate)** as
$$f_\text{err}(\{ y^{(i)},\hat{y}^{(i)} \}_{i=1,\ldots,N})=\frac{1}{N}\sum_{i=1}^{N} \mathrm{I}(y^{(i)}\neq \hat{y}^{(i)})$$
where $N$ is the number of test examples and
$$\mathrm{I}=\begin{cases}
1 & \text{if true} \\
0 & \text{if false}
\end{cases}$$
is an indicator function that turns boolean values into numbers. This function returns a number between 0 and 1, with 1 being a 100% error rate and 0 being a perfect outcome.

[^1]: Be careful with the word "enough". It's not a loose word, "enough" needs to have some real meaning, a specific *threshold* value of $a$ if you wish.

[^2]: For instance, given a seed of an Iris flower of species $y$, nature makes $y$ grow into a Iris $x$ (the process is $y\mapsto x$). Our model instead predicts the species $y$ from the flower $x$ (the process is $x\mapsto y$).

[^3]: If you want to be completely explicit, you can write the signature as $f_\text{IC}:\mathcal{F}_{X\mapsto Y}\times M\times \mathcal{F}_{X\mapsto Y}\mapsto \mathbb{R}$ where we added $M$ to highlight that the comparison depends on the model $m\in M$ your testing.

[^4]: We're assuming that the tests are high-quality and correct. That's another important factor.

[^5]: In other words, we turned a machine learning problem in a fancy [[linear regression]] problem.
