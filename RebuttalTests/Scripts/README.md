## Rseed Test


This scripts folder has 3 files:-

1. `generate_rseed_embeddings.ipynb`:  This generates multiple UMAPs with the input dataset of 31 tutored birds, changing nothing but the seed.

2. `find_kmeans_centroids_of_rseed_embeddings.ipynb`: It computes the centroids for the syllable clusters of the focal birdsong.

3. `bird_paths_from_many_kcentroids.ipynb`: It computes the path length for every birdsong in the multiple UMAPs.


Order of execution:-

1. `generate_rseed_embeddings.ipynb`
2. `find_kmeans_centroids_of_rseed_embeddings.ipynb`
3. `bird_paths_from_many_kcentroids.ipynb`




Note:

- All the tests were conducted on non-normalised UMAP embeddings.
- The cluster labels are a combination of what they provided + kmeans.

