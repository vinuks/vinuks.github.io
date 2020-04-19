---
layout: post
title: Paraphrase detection - Dynamic Pooling and unfolding RAE
date: '2020-04-18 13:02:47 -0700'
categories: jekyll update
published: true
---

[WIP] Dynamic Pooling and Unfolding Recursive Autoencoders for Paraphrase Detection

Paraphrase detection definition

Recursive autoencoders

Requires a parse tree to already be present as part of input

Unfolding RAE vs RAE - difference being the decoding tries to reconstruct entire parse tree (as opposed to only immediate children that were used to construct the final layer)

Unfolding RAE tries to construct the hidden layer such that it represents the entire subtree under it (and not just its children)
Larger the subtree, greater the importance in an Unfolding RAE.

Deep RAE : Can replace the single neural layer with multiple layers.

Computing sentence similarity: 

- Construct phrase vectors and word vectors for the two input sentences A and B
- Compute Similarity matrix, where similarity is computed between every pair a $$\epsilon$$ A, b $$\epsilon$$ B
- Use Min Pooling - helps to fix the size of the input to neural network / classifier. This is lossy, but maintains overall structure.
- Normalize each entry

Add in some handcrafted features
 - Number of Numbers matched
 - Difference in sentence length
 - % Overlap in words / phrases

 They show that Dynamic Pooling + unfolding RAE outperforms all other baselines
 They also empirically show that Dynamic Pooling is the better option for Feature extraction - compared to historgram. They demonstrate importance of handcrafted features.