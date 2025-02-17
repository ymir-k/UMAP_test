## Test #1 Rseed Repeatability - Scripts


This folder has 3 scripts corresponding to Test #1 Rseed Repeatability :-

1. `generate_rseed_embeddings.ipynb`: This script generates multiple UMAPs with the input dataset of 31 tutored birds ("tut.csv"), changing nothing but the seed for the random number generator.

2. `find_kmeans_centroids_of_rseed_embeddings.ipynb`: It computes the centroids of the syllable clusters within each UMAP.

3. `bird_paths_from_many_kcentroids.ipynb`: It computes the path length for every birdsong in the multiple UMAPs.


Order of execution:-

	1. `generate_rseed_embeddings.ipynb`
	2. `find_kmeans_centroids_of_rseed_embeddings.ipynb`
	3. `bird_paths_from_many_kcentroids.ipynb`
	
Note:

- All the tests were conducted on non-normalised UMAP embeddings, similar to Alam et, al.

