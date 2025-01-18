## Test #3: Rseed Test


This scripts folder has 5 files:-

1. `label_rseed_embeddings_df.ipynb`: This updates the embedding csvs to include metadata about the sample point, in addition to just its UMAP coordinates.

2. `generate_rseed_embeddings.ipynb`:  This generates multiple UMAPs with the same input set of 31 birds, changing nothing but the seed.

3. `find_kmeans_centroids_of_rseed_embeddings.ipynb`: It computes the centroids for the syllable clusters of the focal bird.

4. `bird_paths_from_many_kcentroids.ipynb`: It computes the path length for every bird in the multiple UMAPs. This script corresponds to test 3a.

5. `pairwise_distances_from_rseed_kcentroids.ipynb`: It computes the distance between each pair of clusters for each bird in the multiple UMAPs. This script corresponds to test 3b.


Order of execution:-

0. `label_rseed_embeddings_df.ipynb`: This can be skipped as the embedding files with the info are already available in the results folder.

1. `generate_rseed_embeddings.ipynb`
2. `find_kmeans_centroids_of_rseed_embeddings.ipynb`
3. `bird_paths_from_many_kcentroids.ipynb`
4. `pairwise_distances_from_rseed_kcentroids.ipynb`
