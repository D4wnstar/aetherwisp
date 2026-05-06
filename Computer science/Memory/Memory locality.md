---
hl-publish: true
---


### Organizing data to improve locality
Memory locality has many pleasant properties that we want to exploit, so organizing our data in such a way that locality is improved is a goal worth working towards. The data exists in some "data space," which could really be anything: for example, 3D Euclidean space $\mathbb{R}^{3}$, or $\mathbb{R}^{2}$, or anything else depending on what's stored. The data is, probably, not distributed uniformly in this space. In all likelihood, there are *spatial patterns* in this space that we can use to store data in a more efficient manner.