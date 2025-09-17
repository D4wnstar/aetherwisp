---
wiki-publish: true
---
**Time of flight** (**TOF**) is the time it takes for a [[particle]] to travel from one [[detector]] to another, assuming the two detectors are specifically paired to measure the passing of the particle. Calling $t_{1}$ the time of passage at the first detector and $t_{2}$ that at the second one, TOF is simply
$$\text{TOF}=t_{2}-t_{1}$$
The purpose TOF is to determine the speed of the particle. Given a distance $L$ between the detectors, the speed is
$$v=\frac{L}{\text{TOF}}$$
The [[standard deviation]] on this measurement depends on the quality of the TOF measurement. Assuming $L$ has negligible error, we have
$$\frac{\sigma_{v}}{v}=\frac{1}{v} \frac{L\sigma _\text{TOF}}{\text{TOF}^{2}}=\frac{\text{TOF}}{L} \frac{L}{\text{TOF}^{2}}\sigma _\text{TOF}=\frac{\sigma _\text{TOF}}{\text{TOF}}=\frac{v}{L}\sigma _\text{TOF}$$
Assuming the detectors are identical (generally a good idea), the error $\sigma _\text{TOF}$ will be itself given by the error on $t_{1}$ and $t_{2}$ at the source:
$$\sigma _\text{TOF}=\sigma(t_{2}-t_{1})=\sqrt{ \sigma ^{2}_{t_{2}}+\sigma ^{2}_{t_{1}} }=\sqrt{ 2\sigma_{t}^{2} }=\sqrt{ 2 }\sigma_{t}$$
and so
$$\frac{\sigma_{v}}{v}=\sqrt{ 2 } \frac{v}{L}\sigma_{t}$$

> [!example]-
> Suppose our two detectors have $\sigma_{t}=0.1\text{ ns}$. We want to measure a speed of $v=0.5c$ with a relative error $\sigma_{v}/v=1\%$. How far away must they be? Inverting the error law we get
> $$L=\frac{v}{\sigma_{v}}\sqrt{ 2 }v\sigma_{t}=212\text{ cm}$$
> This is the distance needed to get this level of precision with our instrumentation.
