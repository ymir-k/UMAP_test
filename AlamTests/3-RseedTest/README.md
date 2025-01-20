## Testing reliability of global distances between UMAP clusters 
Remya, I wonder whether we shall call this part of repo testing as nothing is tested here. We test everything in R. Instead, I suggest to title this "Generating 20 UMAP iterations for 31 birds of Alam et al Fig. 2c

We test two arguments:

1. Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable.
2. Distances b/w any two clusters are dependent not just on the properties of the samples of these two clusters, but also on the other samples in the dataset. Hence, the pairwise distances are a relative measure, not an absolute one, at best.

REMYA:Not sure whether we need the argumentation, we are generating only the datasets, no?

### Method
-  We use Alam et al's data behind Fig. 2c, available from their repository [here](https://doi.org/10.18738/T8/WBQM4I/Q92O9A)
-  We then use their methods (see [Scripts](Scripts)) to make 20 UMAP embeddings of the same dataset of 31 tutored birds.
-  We change no parameters, except the seed for the random number generator.
-  In each of the UMAP embeddings, we compute
	- a. `path length`
		- for each bird by doing SO AND SO, which gave 31*20=620 path lengths (20 per bird)
		- avaialble at [path_length_df.csv](path_length_df.csv)
	- b. `euclidean distance` b/w each pair of syllable clusters;
		- with 150 syllable clusters, this makes ( 150 x 149 ) / 2  = 11175 pairs and
		- with 20 UMAPs, this gives 11175 * 20 = 223500 pairwise distances in total
		- avaialble at [path_length_matrix.npy](path_length_matrix.npy)

Specific information about these files is provided in the corresponding README.

Note:
- All the tests were conducted on non-normalised UMAP embeddings, exactly as Alam et al did.
- The cluster labels are a combination of what Alam et al provided + kmeans.
