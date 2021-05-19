---
title: 2021-05-18-deep learning chapter15 notes
tags: [deep learning, note]
category: [note]
renderNumberedHeading: true
grammar_cjkRuby: true
---

# Note
## top question
 * what makes one representation better than another?
	 * disentangle the ==underlying causal factors of variation #2196F3== that generated the data.
   

### greedy layer-wise unsupervised pretraining
**greedy layer-wise:**  train one layer at a time, training the k-th layer while keeping the previous ones fixed.
**unsupervised:** each layer is trained with an unsupervised representation learning algorithm.
**pretrain:** it supposed to be only a first step before a joint training algorithm is applied to fine-tune all the layers together.


### two principles
> the choice of the initial arameters for a deep neural network can have a significant regularizing effect on the model

> learning about hte input distribution can help with learning about the mapping from inputs to outputs

### saliency
the fixed criteria determine which causes are considered salient.
other definitions of alience are possible, like **highly recognizable pattern**

### the disadvantages of unsupervised pretraining
1. the supervised objective will regularization the supervised model using a single hyperparameter, while in unsupervised pretraining, here is not a way of flexibly adapting the strength of the regularization.
2. each phase has its own hyperparameter, there is a long delay between proposing hyperparameters for the first phasee and being able to update them using feedback from the second phase.
3. deep learning has a great success in large labeled dataset, while on extremely small datasets. **bayesian methods outperform** methds based on unsupervised pretraining.

### related domains
1. domain adaptation
2. concept drift
3. few-shot learning or zero-shot learning
4. semi-supervised learning
	1. the marginal `!$f(x)$` is intimately tied to the conditional `!$p(y|x)$` 
	2. it is not possible to capture all or most of the factors of variation that influence an observation
	3. what to encode in each situation
	   a. use supervised and self-supervised at the same time for most relevant factors of catiation
	   b. use much larger representations
5. distirbuted representation (this model generate well)
	1. the hidden units can learn to represent the underlyig causal factors that explain the data
	2. induce a rich *similarity space*
	3. the number of regions this binary feature representation can distinguish is as follows. this explain the **generalization power** of the distributed representation.
	```mathjax!
	$$\sum_{j=0}^d\binom{n}{j}=O(n^d)$$
	```
	4.  there is no need to have labels for the hidden unit classifiers: *gradient descent on an objective function of interest naturally learns semantically interesting features.*
		



# SUMMARY
- self supervised learning as a pre-text task is not always helpful.
- we cannot know **exactly** what aspects of the pretrained parameters are retrained during the supervised training stage is limited

# QUESTION
1. how to perform unsupervised learning and supervised learning simultaneously?
	