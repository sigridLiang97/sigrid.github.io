---
title: 2021-05-18 deep learning chapter15 notes
tags: deep learning, note,
category: note
renderNumberedHeading: true
grammar_cjkRuby: true
---


# Note
### greedy layer-wise unsupervised pretraining
**greedy layer-wise:**  train one layer at a time, training the k-th layer while keeping the previous ones fixed.
**unsupervised:** each layer is trained with an unsupervised representation learning algorithm.
**pretrain:** it supposed to be only a first step before a joint training algorithm is applied to fine-tune all the layers together.


### two principles
> the choice of the initial arameters for a deep neural network can have a significant regularizing effect on the model

> learning about hte input distribution can help with learning about the mapping from inputs to outputs

### the disadvantages of unsupervised pretraining
1. the supervised objective will regularization the supervised model using a single hyperparameter, while in unsupervised pretraining, here is not a way of flexibly adapting the strength of the regularization.
2. each phase has its own hyperparameter, there is a long delay between proposing hyperparameters for the first phasee and being able to update them using feedback from the second phase.
3. deep learning has a great success in large labeled dataset, while on extremely small datasets. **bayesian methods outperform** methds based on unsupervised pretraining.

# SUMMARY
- self supervised learning as a pre-text task is not always helpful.
- we cannot know **exactly** what aspects of the pretrained parameters are retrained during the supervised training stage is limited

# QUESTION
1. how to perform unsupervised learning and supervised learning simultaneously?
	