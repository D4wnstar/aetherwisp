---
wiki-publish: true
aliases:
  - FPR
  - TPR
---
The **False Positive Rate** (**FPR**) is a [[performance index]] that states how many negative cases are wrongly classified as positive. Formally:
$$f_\text{FPR}(\{ y^{i},\hat{y}^{i} \}_{i})=\frac{\sum_{i=1}^{N}\mathrm{I}(y^{i}=\text{neg or }y^{i}\neq \hat{y}^{i})}{\sum_{i=1}^{N} \mathrm{I}(y^{i}=\text{neg})} $$
FPR is defined between 0 and 1 (a percentage). If there are no positives, it is undefined (divides by zero). FPR is best when its lowest. It's commonly provided alongside the [[False Negative Rate]].

A more convenient notation is
$$\text{FPR}=\frac{\text{FP}}{\text{N}}$$
where $\text{FP}$ is the number of false positives and $\text{N}$ is the number of negatives. This assumes the presence of a real and predicted set $\{ y^{i},\hat{y}^{i} \}$ even if not written. Counting false positives needs both $y^{i}$ and $\hat{y}^{i}$, whereas counting negatives only need $y^{i}$.

A sibling quantity is the **True Positive Rate**, which is the count of correctly classified positives. It is the complement of FPR:
$$\text{TPR}=1-\text{FPR}$$
Like FPR, TPR is defined on $[0,1]$. You want TPR to be as close to 1 as possible.