# README

This folder has all the scripts to run the various tests on the Alam dataset.

1. `0-TestScripts`: These auxillary scripts were used to test various functions, such as finding shortest path, calculating centroids, etc, before they were used in the tests.

2. `1-SplitComparisonTest`: Scripts and results corresponding to test #1. This test takes one focal bird, puts it in two sets of 15 different birds, and tests the reproducibility of its path length, given different accompanying birds.

3. `2-Permutations_w_focalbird`: Scripts and results corresponding to test #2. This test takes one focal bird, puts it in 10 sets of 5 non-focal birds, and tests the reproducibility of its path length, given different accompanying birds.

4. `3-RseedTest`: Scripts and results corresponding to test #3. This test makes 20 UMAP embeddings of the entire dataset of 31 tutored birds. It changes no parameters, except the seed for the random number generator. It tests the repeatability of the path length for each bird, across multiple UMAP renditions. It also looks at repeatability of pairwise distances for every pair of clusters across UMAP renditions.

5. `4-FlipTest`: Scripts and results corresponding to test #4. This test takes all pairs of birds and checks how consistently the same bird has the longer path length in the pair. It tests if one bird in a pair can be reliably labelled as the one with the relatively longer path.

6. `5-NsyllTest`: Scripts and results corresponding to test #5. This tests the relation of path lengths with number of syllables. This looks at how the path length changes if we form a path using randomly selected k(=2,3,..,8) clusters 50 times in one UMAP. The variability of path length doesn't change with k, but the mean increases with k.