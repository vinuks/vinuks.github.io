---
layout: post
title: Paraphrase detection - Dynamic Pooling and unfolding RAE
date: '2020-04-18 13:02:47 -0700'
categories: jekyll update
published: true
---

Dynamic Pooling and Unfolding Recursive Autoencoders for Paraphrase Detection

### Definitions:

Paraphrase detection - given two sentences, determine if one is paraphrasing the other - meaning that they both convey the same meaning.

Recursive autoencoders - Autoencoders are neural networks that try to predict the input, and in doing so construct an embedding of the input. The recursive part of it is to use a binary parse tree

### Summary: 
The work done in this paper requires a parse tree to already be present as part of input, they don't mention which parser is used.

![image-title-here](/assets/images/parse-tree-rae.png){:class="img-responsive"}

Unfolding RAE vs RAE - difference being the decoding tries to reconstruct entire parse tree (as opposed to only immediate children that were used to construct the final layer - as seen in the figure)

Unfolding RAE tries to construct the hidden layer such that it represents the entire subtree under it (and not just its children) Larger the subtree, greater the importance in an Unfolding RAE. They also consider a Deeper version of the RAE, where they replace the single neural layer with multiple layers.

In order to compute sentence similarity, they follow the following steps: 

- Construct phrase vectors and word vectors for the two input sentences, lets call the phrase and word vectors for one sentence A and the other B.
- Compute Similarity matrix, where similarity is computed between every pair a $$\epsilon$$ A, b $$\epsilon$$ B
- Use Min Pooling - helps to fix the size of the input to neural network / classifier. This is lossy, but maintains overall structure.
- Normalize each entry.

Add in some handcrafted features - mainly because the pooling layer cannot represent these features.
 - Number of Numbers matched (Is essential to get them exactly right, even for paraphrasing)
 - Difference in sentence length
 - Percentage Overlap in words / phrases

 They show that Dynamic Pooling + unfolding RAE outperforms all other baselines. They also demonstrate importance of handcrafted features. The authors also do a qualitative evaluation, by tring to reconstruct the original sentence using the autoencoder.

### Conclusion: 

Overall, this paper's novel contributions are the unfolding of the RAE to the entire tree, and the pooling of similarity matrix in order to get a fixed shape input - which helps with the classification task.