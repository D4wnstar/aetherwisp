---
wiki-publish: true
---
A **machine learning system** or **ML system** is

> [!example] Twitter profiling
> Let's try to make a system that predicts some basic information about a Twitter user based on a tweet. A tweet is a set of 280 characters, some of which probably null. They are encoded in, say, UTF-16. Call it $A^{280}$ where $A$ is a single UTF-16 character. We want to transform this into a very primitive estimate of age range $\{ 0\text{-}18, 19\text{-}24,25\text{-}35,36\text{-}50,51+\}$ and gender $\{ \text{M},\text{F} \}$.
> (Finish this)

### Design process
ML systems are complicated and can take an enormous number of shapes and sizes. It's necessary, or at least very recommended, to take a formulaic approach to designing one in order to enforce some rigor in the logic behind the system. There are many ways one could go about this: here is one path.
1. **Decide whether you even need machine learning.** Though ML is incredibly powerful, in many cases it's just unnecessary. Perhaps the problem is simple enough that it can be solved rigorously and deterministically, especially if a solution already exists. No point in using ML to calculate 17 + 45. Perhaps the problem is so complicated that creating an ML system to approximate a good solution would take more time, hardware or funds than you have available. You *could* determine continent-scale population dynamics using ML, but you would need enormous labor to do so.
2. **Supervised or unsupervised?** [[Supervised machine learning]] is expensive and labor-intensive since you need an enormous amount of curated data designed specifically for your training process. [[Unsupervised machine learning]] instead only requires the raw data and it figures out what to do on its own, but you sacrifice a lot of control over the process and the model can learn to predict the wrong thing[^1].
3. **Define the problem.**
4. **Design the ML system.**
5. **Implement the ML system.**
6. **Assess the ML system.**

Some additional points. Consider some ML system summarized as $f_\text{predict}: X\mapsto Y$.
- Even if you do make the ML system, can $y$ be calculated fast enough for your purposes? Would a human be able to do it faster or more accurately?
- If a human can do it, why not? Cost? No available workers? Danger to the person (e.g. chance of collapse of an abandoned building)? Inherent bias to the human? $y$ is not high-value enough to justify getting a person to do it?
- While $f_\text{predict}$ is expected to be derived using machine learning, nothing's stopping a person from estimating the function themselves. If, say, a physicist can hand-make a competent model or theory for a phenomenon, you don't necessarily need ML. The question then becomes: is the hand-made solution better than the ML one? For instance, is the human solution too expensive, time-consuming or inaccurate?

By and large, you could oversimplify the design philosophy of an ML systems down to three metrics:
- **Efficiency.** How fast and easily does the ML system runs? Are the resources used justified?
- **Effectiveness.** How good are the decisions made by the ML system? Are they good enough for your purposes?
- **Human dignity.** Would a human do the same thing better? Would the ML system encourage damaging behavior?[^2]

> [!example] Iris classification
> Let's unearth the good-old Iris dataset for an example. You have data on three kinds on Iris flowers. Normally that's petal and sepal lengths, but let's assume you have the actual flowers and can do whatever you want with them. Some of them are classified and some aren't. You want to classify all the remaining ones. You're doing this just for fun and want to figure out how to classify the flowers. Let's design an ML system to do so.
> 
> **Do you need machine learning?**
> You *could* go to a professional botanist and have them classified, but let's be real, you're not spending that kind of money just for fun. But also, you aren't a botanist yourself. You don't know how to classify the flowers manually. So if you can't do it and don't have someone else to do it for you for free, you don't have much of a choice: ML seems to be the answer. Let's be more precise. Do we need fast speeds? No, we've got time to wait. Do we need high precision? It's a nice-to-have, but probably not, quality can afford to be "good enough" for a for-fun side project.
> 
> **Supervised or unsupervised?**
> Well, we already have the input-output pairs (petal/sepal lengths to iris type), so it's an easy decision: supervised it is. If you didn't have the pairs, you'd probably need to go for unsupervised since you're unwilling to pay for classification (i.e. training data generation).
> 
> **Define the problem.**
> A simple form of the problem is: given an Iris flower, give me its species. Formally, this means turning $X=\{ x:x\text{ is an Iris flower} \}$ into $Y=\{ \text{setosa},\text{versicolor},\text{virginica} \}$. This is a might be complicated problem though. Why? Because $X$ is not in a shape that is particularly suitable for the problem, primarily because it's a set of literal, physical flowers. The information is there, but it's not easily accessible in this form. We can't change the raw source, that's just the flowers that we have, but what we can do is preprocess $X$ (the flowers) to turn it into a more suitable $X'$ that can be input into a machine learning method. In our case, we need to turn physical flowers into digital information about them. Formally, this means adding a function $f_\text{preprocess}:X\mapsto X'$. So the new question is: how do we make $f_\text{preprocess}$? Do we also use ML for this? If so, we might want to go through the whole design process for preprocessing too, though that's a bit overkill. We should just question if $f_\text{preprocess}$ is low-cost enough to justify using and then decide accordingly. How much information is retained by preprocessing? How much more useful is $X'$ really over $X$? Most importantly, $X'$ needs to be directly applicable to one or more machine learning techniques; the more the better.
> 
> In our case, $f_\text{preprocess}$ depends on what the original $X$ is. We have some flowers but we are free to take whatever measurements we want on them. Some examples:
> - You can describe the flower if very good detail. $x'\in X'$ is a text description of the element $x \in X$. $f_\text{preprocess}$ is a captioning function that takes the flower and describes it. You can do it yourself or get a vision-language model to caption photos of the flower.
> - You can digitalize photos of the flowers. $x'\in X'$ is a very rough 512x512 RGB image of the flower, meaning a $[0,1]^{512\times 512\times 3}$ array. You can take the photos yourself and filter the images to this array with traditional programming.
> - You can measure some aspects of the flower, like the usual petal and sepal lengths and widths. $X'$ can be a lot of things here depending on what you measure, but is probably going to be some form of $\mathbb{R}^{N}$ where $N$ is the number of physical properties you measure per flower.
> - Ludicrously, you could sequence the genome of each flower and get a string of [[nucleotide base|nucleotide bases]], then train the ML model on these. Technically speaking, you can't get more precise than this, but it's comically expensive and just overkill. Here, $X'$ would be an $\{ \text{A,C,T,G} \}^{N}$ string, where $N$ is the length of the genome and $\text{A,C,T,G}$ are [[adenine]], [[cytosine]], [[thymine]] and [[guanine]] respectively.
### Components
ML systems are made up of many components. The difference between a system and a simple ML model is that the system also includes all accessory code and methods that combine to turn an input into a decision. It may include multiple models strung together. So what are these components?

[^1]: An anecdote: an MLOps professor of mine was working on a system to make predictions on photos of places in different districts of a Brazilian city. If I recall correctly, it was suppose to determine which district the image was taken in. Instead of doing that, the unsupervised model instead learnt to categorize the images based on the time of day... If you're doing unsupervised learning, perhaps invest in [[explainable AI]].

[^2]: For instance, an unsupervised ML system that spontaneously learns to discriminate based on race or gender.
