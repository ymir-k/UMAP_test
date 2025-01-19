# README



Here, we test the repeatability and reproducibility of using euclidean distances between clusters in a UMAP embedding.

We do this using two datasets:-
1. Alam dataset: The dataset of zebra finch songs provided by Alam et al., 2024.
2. MNIST dataset: The publicly available dataset of handwritten digits (http://yann.lecun.com/exdb/mnist/).


In both the datasets, we see that the euclidean distance between any pair of UMAP clusters has a repeatability of ~0.1 across multiple UMAP embeddings.

The path length between k clusters is defined as the sum of euclidean distances between each pair of clusters in the shortest path connecting them.

The path length has a higher repeatability (~55%), but this drastically diminishes when accounted for the number of clusters in the path.

Also, the path length of a given set of clusters changes when the input dataset to the UMAP is changed, i.e. path length has a low reproducibility.

Further, the tests on the Alam dataset show that path lengths of two birds cannot be compared within a single UMAP embedding. A birdsong with the longer path length in one UMAP embedding can very well have the shorter path length in another UMAP embedding, where only the seed is changed (`FlipTest`).

