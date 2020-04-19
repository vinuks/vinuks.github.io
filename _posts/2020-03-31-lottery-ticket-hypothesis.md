---
layout: post
title: Lottery ticket one
date: '2020-03-31 23:02:47 -0700'
categories: jekyll update
published: true
---

## Lottery ticket Hypothesis

This paper introduces the idea that given a trained complex neural network, one can find a smaller network (called lottery tickets) that when trained in isolation can match the test accuracy of the larger network with the same initialization and number of iterations of training.

The procedure for identifying a lottery ticket is to init a network with weights $$\theta$$, iteratively train a network and prune some percentage $$p$$ of the parameters, and then retrain the remaining parameters with the same initialization in $$\theta$$.

Random initializations with the pruned network does not reproduce the results - indicating that the structure alone cannot explain the lottery ticket's success. They suggest that understanding lottery tickets can help mprove training performance, design better networks and improve theoretical understanding of networks.

The paper does hypothesize that the structure of the winning tickets do encode an inductive bias customized to the learning task at hand. 
As the pruning increases, the test accuracy goes up and then down. They seemed to have focused only on vision based classifications using a CNN and a fully connected neural network.

However, all of the work done is empirical and does not seem to have any theoretical proofs / guarantees of lottery tickets existence. Also the paper focuses primarily on vision centric classification tasks on smaller datasets.

Terminology: Dropout, Weight decay, Batchnorm, Residual connections. 
