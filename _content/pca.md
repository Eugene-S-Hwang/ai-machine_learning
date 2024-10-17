---
layout: page
title: "Understanding PCA"
permalink: /pca
---
# Principal Component Analysis (PCA) for beginners

PCA is a cool way of simplifying complex data while keeping its most important parts. Let's understand it in a easy way.

## What is PCA?
PCA is useful because it helps us reduce the complexity of data. Imagine you have a dataset with 10 or even 100 variables. PCA helps by reducing it to just a few key principal components that capture most of the important information.

I have learned PCA for my natural language processing (NLP) project to visualize the word embeddings. Word embeddings are ways of representing words as vectors of numbers so that we can do calculations with them.
Imagine we have a set of word embeddings for four words: "king", "queen", "man", and "woman". Each word is represented by a vector in a high-dimensional space (e.g., 300 dimensions). The vectors might look like this (simplified to 2 dimensions for our example):


| Word   | x-coordinate | y-coordinate |
|--------|--------------|--------------|
| king   | 2            | 5            |
| queen  | 3            | 5            |
| man    | 1            | 4            |
| woman  | 2            | 4            |

When we plot these points, we may notice that the words "king" and "queen" are somewhat similar, and the words "man" and "woman" are also similar. However, it’s still hard to visualize their relationships in high-dimensional space.

Using PCA, we can reduce the dimensions from 300 to just 2, which makes it easier to visualize. PCA will find the two directions (principal components) where the word vectors vary the most. Typically, the first principal component might capture the difference between gender (e.g., "man" vs. "woman"), while the second principal component might capture royalty (e.g., "king" vs. "queen").

After applying PCA, we can create a new plot where the words are positioned based on these new principal components. This makes it easier to see relationships like how "king" and "queen" are similar to "man" and "woman", with a similar difference vector between them.

## Visualizing Higher Dimensions

In 2 dimensions, we can visualize points using an x-y coordinate plane. For example, if we have two points, we can easily plot them on a graph. In 3 dimensions, we add a z-axis, and we can visualize points in a 3D space, like in a cube.

But what if we have 4 or more dimensions? Visualizing 4D, 5D, or higher dimensions becomes impossible to do directly because our brains are not used to perceiving more than 3 dimensions. This is where PCA becomes super helpful. PCA allows us to project higher-dimensional data into 2 or 3 dimensions, making it easier to visualize while retaining as much important information as possible.

For example, if we had a dataset with 4 variables—let’s say height, weight, age, and income—each person would be a point in a 4-dimensional space. Instead of trying to imagine 4D space, we could use PCA to reduce the dataset to 2 dimensions. PCA would create two new variables (principal components) that capture most of the variation in the data. We could then plot these two components on an x-y plane, allowing us to see patterns and relationships that would be impossible to visualize otherwise.

## What Does This Mean?

The eigenvector corresponding to the largest eigenvalue tells us the direction in which our data has the most variance. In the case of word embeddings, it means that we can identify the most important dimensions that capture relationships among words, such as gender or type (e.g., royalty).

We can now project our original data (word vectors) onto these new directions, which helps reduce the dimensionality while still keeping the most important information about the relationships between words.



## References

1. Géron, A. (2019). **Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow** (2nd ed.). O'Reilly Media.
2. Wikipedia contributors. (2024). **Principal component analysis**. *Wikipedia, The Free Encyclopedia*. Retrieved from https://en.wikipedia.org/wiki/Principal_component_analysis

> Note: Some of the content in this blog post was written with the help of ChatGPT, an AI language model by OpenAI.

