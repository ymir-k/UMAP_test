# README

This folder has the scripts used in `Bulla, et al 2025` to generate the UMAPs from the `Alam et. al 2024` dataset.

We test the repeatability of the path length for each birdsong, across multiple UMAP renditions.


## Testing global distances between UMAP clusters

We test the following argument:

- Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable. The path length metric is based on a summation of the distances between these clusters. Hence, the reliability of this metric is questionable.


### `Rseed Test`

#### Test description

Here, you will find the description of the test we run to examine this argument.


	-  In this test, we make 20 UMAP embeddings of the same dataset of 31 tutored birds.
	-  We change no parameters, except the seed for the random number generator.
	-  In each of the UMAP embeddings, we compute the path length for each bird.
	-  This gives 31*20=620 path lengths, 20 per bird.
	-  Separately, in R, we check the repeatability of the path length of a bird, across diff seeds for the random number generator.



#### Test reproducibility

For reproducing the results,
the scripts related to these tests are in the folder `Scripts`.


#### Test results


The `Results` folder has 3 main files:-
1. `path_length_df.csv`
	- This csv file has the path lengths for each birdsong across 20 UMAP embeddings.
	- This has all the data needed to compute repeatability.
	- The columns `kdistance` has the relevant path lengths.
	- Specific details provided in the results folder.
2. `path_length_matrix.npy`
	- Matrix representation of `kdistance` for easy loading into python.
3. `path_length_vs_iter.png`
	- Plot to visualise the csv.
	- The path lengths across 20 UMAP embeddings is plotted for each birdsong.
	
Specific information  about  these  files is provided in the corresponding README.

