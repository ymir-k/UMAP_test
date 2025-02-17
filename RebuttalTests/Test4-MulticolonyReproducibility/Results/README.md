## Test #4 Multi-colony Reproducibility - Results



This folder has the results corresponding to Test #4 Multi-colony Reproducibility :-

1. `path_length_df.csv`
	- This has all the data needed to compute repeatability.
	- The column `kdistance` has the relevant path lengths.
	- The columns `focal_bird_id`, `combo_no` and `kdistance` are the ones most relevant for computing repeatability.
	- Column description:
	
			- focal_bird_id: 0-31; bird being tested
			- combo_no: 0-9; nth sample of 5 birds chosen from the 30 leftover birds
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
	- distance_matrix[focal_bird_id, combo_no] = kdistance




3. `path_length_vs_split.png`

	- Plot to visualise the csv.
	- path length (`kdistance`) vs `focal_bird_id`
	- y-axis: The shortest path length b/w the syllable clusters of the focal bird.
	- x-axis: Focal bird id.
	- 10 path lengths per bird, generated from the subset UMAPs.
	- The subset UMAPs are formed using the focal bird + 5 randomly chosen non-focal birds.
	