## Testing global distances between UMAP clusters

We test two arguments:

1. Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable.

2. Distances b/w any two clusters are dependent not just on the properties of the samples of these two clusters, but also on the other samples in the dataset. Hence, the pairwise distances are a relative measure, not an absolute one, at best.

Here, you will find the first test.

1. `Split Comparison Test`

	- In this test, we use 31 tutored birds from the Alam dataset.
	- 1 bird is chosen as the focal bird.
	- The 30 non focal birds are randomly split into two, with 15 birds each.
	- This makes 2 subsets of 16 birds each, both containing the focal bird.
	- We generate the UMAP embeddings for these 2 subsets with the given focal bird.
	- We compute the path length of the focal bird in these 2 UMAPs.
	- Then, we repeat this for each of the 31 birds.
	- This generates 31*2=62 path lengths, 2 each per bird.
	- Separately, in R, we check the reproducibility of the path length of a bird, given different neighbours.


The scripts related to these tests are in the folder `Scripts`.

The `Results/KDistances` folder has 3 files:-
1. `path_length_df.csv`
	- This has all the data needed to compute repeatability.
	- The columns `kdistance` has the relevant path lengths.
2. `path_length_matrix.npy`
	- Matrix representation of `kdistance` for easy loading into python.
3. `path_length_vs_iter.png`
	- Plot to visualise the csv.
	
Specific information  about  these  files is provided in the corresponding README.




Note:

- All the tests were conducted on non-normalised UMAP embeddings.
- The cluster labels are a combination of what they provided + kmeans.