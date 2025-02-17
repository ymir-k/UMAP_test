 ## Test #2 Misclassification

In the article `No support for honest signalling of male quality in zebra finch song; Bulla, Sankar, Forstmeier, 2025`, we test the reliability of the path length metric, as described in [Alam et al. (2024, Nature)](https://doi.org/10.1038/s41586-024-07207-4).

We test the path length metric in various contexts, one of which is described in this folder.
We provide here the corresponding scripts and results.


We test this argument:

- Is it the same birdsong in a pair that has the longer path length across all UMAP renditions? i.e. Is the path length comparison repeatable?


#### Test description


Here, you will find the description of the test we run to examine the above argument.


	- In this test, we use the 31 tutored birds from the Alam dataset ("tut.csv").
	- For each birdsong, we have generated their path lengths in 20 UMAP renditions ("Data/path_length_df.csv").
	- We form all possible pairs of birdsongs (= 31 * 30 / 2).
	- For each bird pair, we compare their path lengths across the 20 UMAPs. 
	- We test if the bird in the pair with the longer path length is consistent, i.e. we calculate the probability that the bird in the pair with the longer path length is switched by only changing the UMAP seed.
	- The repeatability of the valence of the path length comparison in bird pairs is further tested separately in R.



#### Test input


The folder `Data` has 1 file which is used as input:-
1. `path_length_df.csv`
	- This file has the path length information for each birdsong in each UMAP rendition.
	- This was computed in previous test `Test #1 Rseed Repeatability`.



#### Test reproducibility

For reproducing the results,
the python scripts related to this test are in the folder `Scripts`.


#### Test results


The folder `Results` has the relevant results for this test.
	
Specific information  about  these  files is provided in the corresponding README.

