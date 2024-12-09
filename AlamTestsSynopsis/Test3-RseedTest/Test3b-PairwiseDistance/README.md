## Test #3b




This test folder has 3 files:-
1. `pairwise_distance_df.csv`
	- This has all the data needed to compute repeatability.
	- The column `kdistance` has the relevant path lengths.
	- The columns `cluster1`, `cluster2`, `iteration` and `kdistance` are the ones most relevant for computing repeatability.
	- Columns:
		- cluster1: 0-149; 1 of the 2 syllable clusters being tested
		- cluster2: 0-149; 1 of the 2 syllable clusters being tested
		- iteration: 0-19; nth UMAP embedding with a diff random state
		- rseed: 0-1e8; seed used for the corresponding UMAP embedding
		- distance: path length based on their cluster labels
		- kdistance: path length based on improved cluster labels
		- range_0_min: min(x), UMAP embedding range, useful for normalising
		- range_1_min: min(y), UMAP embedding range, useful for normalising
		- range_0_max: max(x), UMAP embedding range, useful for normalising
		- range_1_max: max(y), UMAP embedding range, useful for normalising



2. `pairwise_distance_matrix.npy`

	- Matrix representation of `kdistance` for easy loading into python.
	- distance_matrix[cluster1, cluster2, n_iter] = kdistance




3. `pairwise_cluster_distances.png` and `pairwise_cluster_distances.svg`

	- Plot to visualise the csv.
	- `kdistance` vs `cluster pair`
	- y-axis: The distance b/w the pair of syllable clusters.
	- x-axis: Cluster pair
	- 20 path lengths per cluster pair, generated from the UMAPs with diff random states.
	- The 20 UMAPs are formed changing no parameter, except the seed of the random number generator.
	