## Test #1 Rseed Repeatability - Results



This folder has the results corresponding to Test #1 Rseed Repeatability :-

1. `path_length_df.csv`
	- The csv file contains the path lengths for each birdsong within the 20 UMAP embeddings.
	- It has all the data needed to compute repeatability.
	- The column `kdistance` has the relevant path lengths.
	- The columns `focal_bird_id`, `iteration` and `kdistance` are the ones most relevant for computing repeatability.
	- Column description:
	
			- focal_bird_id: 0-31; bird being tested
			- iteration: 0-19; nth UMAP embedding with a diff random state
			- rseed: 0-1e8; seed used for the corresponding UMAP embedding
			- distance: path length based on their cluster labels
			- kdistance: path length based on improved cluster labels
			- n_syll: number of syllable clusters corresponding to focal bird
			- non_focal_birds: ids of the non focal birds included  in this subset
			- range_0_min: min(x), UMAP embedding range, useful for normalising
			- range_1_min: min(y), UMAP embedding range, useful for normalising
			- range_0_max: max(x), UMAP embedding range, useful for normalising
			- range_1_max: max(y), UMAP embedding range, useful for normalising



2. `path_length_matrix.npy`

	- Matrix representation of path length (`kdistance`) for easy loading into python.
	- distance_matrix[focal_bird_id, n_iter] = kdistance




3. `path_length_vs_seed.png`

	- Plot to visualise the csv.
	- Path length (`kdistance`) vs `focal_bird_id`
	- y-axis: The shortest path length b/w the syllable clusters of the focal bird.
	- x-axis: Focal bird id.
	- The plot displays 20 path lengths per bird, generated from the UMAPs with diff random states.
	- The 20 UMAPs are formed changing no parameter, except the seed of the random number generator.
	