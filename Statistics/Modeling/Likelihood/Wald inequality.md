---
wiki-publish: true
---
The **Wald inequality** is an inequality related to the [[likelihood]] function. It states that if $\theta_{t}$ is the [[true value]] of a [[Statistics/Modeling/Model|model]] parameter $\theta$, then
$$\text{E}_{\theta_{t}}[\log \mathcal{L}(\theta_{t};\mathbf{X})]>\text{E}_{\theta_{t}}[\log \mathcal{L}(\theta;\mathbf{X})]$$
for all $\theta\neq \theta_{t}$ and where $\mathbf{X}$ is the [[random variable]] that generated the [[sample]]. The [[Expected value]] of the log-likelihood of the true value is always higher than any non-true value.

This inequality can be proven using [[Jensen's inequality]].