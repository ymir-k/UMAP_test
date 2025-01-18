## Testing global distances between UMAP clusters

We test two arguments:

1. Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable.
2. Distances b/w any two clusters are dependent not just on the properties of the samples of these two clusters, but also on the other samples in the dataset. Hence, the pairwise distances are a relative measure, not an absolute one, at best.

Here, you will find the third test.

3. `Rseed Test`

	-  In this test, we make 20 UMAP embeddings of the same dataset of 31 tutored birds.
	-  We change no parameters, except the seed for the random number generator. 
	
	- a. `Path length`
		- In each of the UMAP embeddings, we compute the path length for each bird.
		- This gives 31*20=620 path lengths, 20 per bird.
		- Separately, in R, we check the repeatability of the path length of a bird, across diff seeds for the random number generator.
	- b. `Pairwise distance`
		-  In each of the UMAP embeddings, we compute the euclidean distances b/w each pair of syllable clusters.
		- With 150 syllable clusters, this makes ( 150 x 149 ) / 2  = 11175 pairs.
		- With 20 UMAPs, this gives 11175 * 20 = 223500 pairwise distances in total.
		- Separately, in R, we check the repeatability of the pairwise distance b/w 2 given clusters, across diff seeds for the random number generator.


The scripts related to these tests are in the folder `Scripts`.



The `Results/KDistances` folder has 3 main files:-
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

