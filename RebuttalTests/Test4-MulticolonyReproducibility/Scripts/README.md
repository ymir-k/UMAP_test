## Test #4 Multi-colony Reproducibility - Scripts



This folder has 3 scripts corresponding to Test #4 Multi-colony Reproducibility :-


1. `generate_perm_embeddings.ipynb`: This script generates the relevant UMAPs. For each focal bird, it creates multiple UMAPs with 5 birds each in addition to the focal bird.

2. `find_kmeans_centroids_of_perm_embeddings.ipynb`: It computes the centroids for the syllable clusters of the focal bird.

3. `bird_paths_from_perm_kmeans_centroids.ipynb`: It computes the path length for the focal birdsong in the corresponding UMAPs.


Order of execution:-

	1. `generate_perm_embeddings.ipynb`
	2. `find_kmeans_centroids_of_perm_embeddings.ipynb`
	3. `bird_paths_from_perm_kmeans_centroids.ipynb`
