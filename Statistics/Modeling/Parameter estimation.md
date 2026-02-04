---
wiki-publish: true
aliases:
  - fit
---
**Parameter estimation** is the statistical technique of finding a set of parameters for a statistical [[model]] that makes the model best **fit** a [[sample]] of data. It is also called **fitting** (data to a model).

Given some initial data $X$ (could be one or more [[Random variable|random variables]]), we want to find the parameters $\theta_{1},\ldots,\theta_{N}$ such that a function $f(X;\theta_{1},\ldots,\theta_{N})$ minimizes some quantity with respect to $X$.

A key concept in estimation is the idea of **repeated replication of the data-generating process**. The idea is that the process that produce the data that we are estimating can be repeated with consistent results. For instance, if you run a survey on 1000 random people, you can run the survey again 1000 more random people and get consistent results. This is important because estimation relies on repeating data generation in order to progressively improve the estimator on each repetition; if the process can't be replicated, this methodology stops making sense. This concept is applicable even in data that's inherently impossible to regenerate, like data reliant on a time period, since we can run artificial simulations.

Parameter estimation may return a specific value for the parameters or an interval. These are respectively called **point estimation** and **interval estimation**.