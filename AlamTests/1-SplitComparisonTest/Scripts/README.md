## Test #1: Split Comparison Test


This scripts folder has 5 files:-

1. `generate_split_embeddings.ipynb`: This generates the relevant UMAPs. For each focal bird, it creates two subsets of 15 birds each plus the focal bird. It generates two UMAPs per focal bird with these input subsets.

2. `find_centroids_of_split_embeddings.ipynb`: It computes the centroids for the syllable clusters of the focal bird.

3. `find_kmeans_centroids_of_split_embeddings.ipynb`: It computes more accurate centroids for the syllable clusters of the focal bird.

4. `bird_paths_from_split_centroids.ipynb`: It computes the path length for the focal bird in the two corresponding UMAPs.

5. `bird_paths_from_split_kmeans_centroids.ipynb`: It computes the path length, using the more accurate centroids, for the focal bird in the two corresponding UMAPs.


Order of execution:-

1. `generate_split_embeddings.ipynb`
2. `find_kmeans_centroids_of_split_embeddings.ipynb`
3. `bird_paths_from_split_kmeans_centroids.ipynb`

OR

1. `generate_split_embeddings.ipynb`
2. `find_centroids_of_split_embeddings.ipynb`
3. `bird_paths_from_split_centroids.ipynb`

