---
wiki-publish: true
aliases:
  - ML
---
**Machine learning** (**ML**) is the science of getting computers to take decisions without telling them how to take them. It is an expansive collection of theory and techniques that explores the mathematical foundations of learning, modeling and making decisions entirely from data and entirely by machines, without being directly instructed by humans. It is a very wide field connecting many fields, like statistics, mathematics, physics, psychology, neuroscience, computer science and more.
## Formalism
At heart, machine learning is about making decisions. Or rather, getting a machine to do them for you. There is some input question and you want the computer to answer for you. Let's formalize this idea: call $x$ the **observation**[^1], which is what's known to the model in order to take a decision. Then, the machine must follow some procedure to compute the **response** or **output** $y$; this procedure is represented by some function $f(x)$. Generally speaking, the decision-making process is, very simply
$$y=f(x)$$
meaning, applying some procedure $f$ on the observation $x$ gives a response $y$. $x$ belongs to the space of all possible observations $X$ and $y$ to the space of all possible responses $Y$. Then the procedure links these two spaces: $f:X\mapsto Y$.

The end goal of machine learning is to provide the machine an algorithmic method to figure out $f$ by itself. We provide the observations, sometimes we also provide responses as examples, and then the machine learns how to connect $X$ to $Y$. In other words, it invents $f$ *autonomously*. It's common to call this function $f_\text{predict}$, because it predicts a response from an observation.

> [!example] Spam emails
> A simple but realistic application of machine learning is in determining whether an email is spam or not. In this case, $X$ is the set of all possible emails, while $Y$ is the set $\{ \text{spam}, \text{not spam} \}$. The procedure $f_\text{predict}$ needs to take an email $x \in X$ and return a decision $y\in Y$.

The fundamental problem of machine learning then isn't to predict $y$ from $x$, but rather getting the *machine* to autonomously *learn* a procedure $f_\text{predict}$ that will do so. In mathematical terms, the problems is to find an $f_\text{predict}$ that does what we want in the space $\mathcal{F}_{X\mapsto Y}$ of all functions that go from $X$ to $Y$.

> [!tip] Fundamental problem of machine learning
> Get a machine to autonomously find an $f_\text{predict}\in \mathcal{F}_{X\mapsto Y}\equiv \{ \text{all functions }f:X\mapsto Y \}$ that maps observations to desired responses.

Now that we have a formal definition of the problem, it's time to look for a solution. How do we get a machine to learn? How do we explore the space $\mathcal{F}_{X\mapsto Y}$ to find our $f_\text{predict}$?

Well, as it happens, there's a *lot* of ways. This shouldn't be that surprising considering that, if you think about it, the fundamental problem is actually incredibly vague and broad. As such, it accepts many, many solutions, each with their pros and cons. But the most straight-forward and intuitive one is to get the model to learn by example: this is called **[[supervised machine learning]]**, referring to the fact that the machine learns from curated, supervised examples. Another major paradigm is its opposite: **[[unsupervised machine learning]]**, where the model is just given a lot of observations with no desired responses and is expected to draw conclusions about them by itself. These two are, by-and-large, the two major branches of machine learning.

[^1]: It goes by many names: observation, input, instance, data point...
