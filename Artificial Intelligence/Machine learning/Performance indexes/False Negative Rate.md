---
hl-publish: true
aliases:
  - FNR
  - TNR
---
The **False Negative Rate** (**FNR**) is a [[performance index]] that states how many positive cases are wrongly classified as negative. Formally:
$$f_\text{FNR}(\{ y^{i},\hat{y}^{i} \}_{i})=\frac{\sum_{i=1}^{N}\mathrm{I}(y^{i}=\text{pos or }y^{i}\neq \hat{y}^{i})}{\sum_{i=1}^{N} \mathrm{I}(y^{i}=\text{pos})} $$
FNR is defined between 0 and 1 (a percentage). If there are no negatives, it is undefined (divides by zero). FNR is best when its lowest. It's commonly provided alongside the [[False Positive Rate]].

A more convenient notation is
$$\text{FNR}=\frac{\text{FN}}{\text{P}}$$
where $\text{FN}$ is the number of false negatives and $\text{P}$ is the number of positives. This assumes the presence of a real and predicted set $\{ y^{i},\hat{y}^{i} \}$ even if not written. Counting false negatives needs both $y^{i}$ and $\hat{y}^{i}$, whereas counting positives only need $y^{i}$.

A sibling quantity is the **True Negative Rate**, which is the count of correctly classified negatives. It is the complement of FNR:
$$\text{TNR}=1-\text{FNR}$$
Like FNR, TNR is defined on $[0,1]$. You want TNR to be as close to 1 as possible. TNR is also called **specificity**, because it measures how precisely the model can tell you what's wrong. This term is more common in diagnostic tests.

FPR is related to the error rate and accuracy of a binary classifier by
$$\begin{align}
\text{Err}&=\frac{\text{FP}+\text{FN}}{\text{N}+\text{P}}=\frac{\text{P}\cdot\text{FNR}+\text{N}\cdot\text{FPR}}{\text{N}+\text{P}} \\
\text{Acc}=1-\text{Err}&=\frac{\text{TP}+\text{TN}}{\text{N}+\text{P}}=\frac{\text{P}\cdot\text{TPR}+\text{N}\cdot\text{TNR}}{\text{N}+\text{P}}
\end{align}$$
