---
title: 2021-05-18 deep learning chapter15 notes
tags: deep learning, note,
category: note
renderNumberedHeading: true
grammar_cjkRuby: true
---



### greedy layer-wise unsupervised pretraining
**greedy layer-wise:**  train one layer at a time, training the k-th layer while keeping the previous ones fixed.
**unsupervised:** each layer is trained with an unsupervised representation learning algorithm.
**pretrain:** it supposed to be only a first step before a joint training algorithm is applied to fine-tune all the layers together.
