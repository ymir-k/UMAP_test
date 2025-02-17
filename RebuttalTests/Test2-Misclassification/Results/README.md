## Test #2 Misclassification - Results



This folder has the results corresponding to Test #2 Misclassification :-


1. `path_length_diff.csv`:
	- The csv file contains the difference in path lengths for each bird pair across the 20 UMAP embeddings.
	- It has all the data needed to compute repeatability.
	- The columns `bird1`, `bird2`, `iteration` and `path_length_diff` are the ones most relevant for computing repeatability.
	- Column description:
	
			- bird1: 0-31; one of the birds in the pair being tested
			- bird2: 0-31; one of the birds in the pair being tested
			- iteration: 0-19; nth UMAP embedding with a diff random state
			- path_length1: path length of the song of bird1 in the corresponding UMAP embedding
			- path_length2: path length of the song of bird2 in the corresponding UMAP embedding
			- path_length_diff: difference in the path lengths of the two birdsongs in the pair
			- n_syll1: number of syllable clusters corresponding to bird1
			- n_syll2: number of syllable clusters corresponding to bird2
			- n_syll_diff: difference in the number of syllables of the two birdsongs in the pair
			- path_length_bysyll1: Path length (path_length1) of the song of bird1 normalised by its syllable count (n_syll1)
			- path_length_bysyll2: Path length (path_length2) of the song of bird2 normalised by its syllable count (n_syll2)
			- path_length_bysyll_diff: difference in the normalised path lengths of the two birdsongs in the pair


2. `path_length_diff.png` and `path_length_diff.pdf`: These plots display the path length difference of each pair across multiple UMAP renditions.

3. `path_length_bysyll_diff.png` and `path_length_bysyll_diff.pdf`: This displays the path length difference of each pair of birdsongs across multiple UMAP renditions, but normalised by the difference in their number of syllables.

4. `prop_by_bird.csv`:
	- The csv file contains the proportion that each bird has the longer path length across pairs and UMAPs.
	
			- bird: 0-31; one of the birds in the pair being tested
			- n_syll: number of syllable clusters for this birdsong
			- prop: proportion of UMAP renditions in which this birdsong has a longer path length than the other birdsong in the pair.

5. `prop_by_nsyll.png`:  This shows the proportion that each bird has the longer path across pairs and UMAPs.

6. `prop_by_nsylldiff.png`:  This shows the proportion that one bird in each bird pair has the longer path as a function of the difference in their number of syllables.

