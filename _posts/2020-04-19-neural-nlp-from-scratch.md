---
layout: post
title: Neural NLP - from scratch
date: '2020-04-19 13:02:47 -0700'
categories: jekyll update
published: true
---

### Natural Language Processing (Almost) from Scratch

[Link](http://www.jmlr.org/papers/volume12/collobert11a/collobert11a.pdf){:target="_blank"}

### Definitions:

Part of Speech tagging:
Chunking:
Named Entity Recognition:
Semantic Role Labeling:

### Summary:

Main goal of paper is to try and excel on multiple tasks and benchmarks while avoiding task specific engineering. They cite that most of the research done until then was focussed on trying and solving specific tasks, as opposed to learning a general internal representation of the language.

The four benchmark tasks are as follows: Part of speech tagging (POS), Chunking (CHUNK), Named Entity Recognition(NER), Semantic Role Labeling(SRL)

The authors mention that the baselines they plan to compare against are only the top existing systems that have avoided using external data (to optimize for specific tasks). 

The authors argue that the traditional approaches for any NLP task involve the following:
 -  Extract hand design features
 -  Choice of features is empirical - based on linguistic intuition, trial and error and task dependent.
This means that each task requires additional research and for tasks that are "complex" the computational cost of computing large number of features might be too high.

The proposal from the authors is to use a multilayered NN that trains from end to end. The deeper layers are automatically tuned towards each specific task.


### Conclusion:

### Tags:



