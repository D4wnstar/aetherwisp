---
wiki-publish: true
---
A **model**, in the context of [[machine learning]], is a set of machine-chosen parameters that complete a hand-made [[template]] function that can then be used to infere predictions. The combination of a model $m$ and its template $f'(x,m)$ provides a prediction function $f_\text{predict}(x)=f'(x,m)$. When using template-based learning, the template is chosen by hand, so finding a model for it becomes the end goal of the machine learning process.

A model is obtained by running a template-based learning technique on a [[Dataset|learning set]]. The model is said to be **learned**, **trained** or **fitted** on the dataset. Formally, the model is one output of the learning technique, as an element $m$ of the space of all possible sets of parameters $M$. Informally, the term is also often used to refer to a still-untrained set of parameters (e.g. "train a model")[^1].

[^1]: Learning techniques also don't have a well-defined end, so determining what counts or doesn't count as an output is a fool's errand. Does one step of training some random initial parameters count as making a model? The convenient answer is "who cares; all sets of parameters are models, but some models are better than others."
