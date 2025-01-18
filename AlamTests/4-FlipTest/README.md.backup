## Testing global distances between UMAP clusters

We test one argument:

1. Is it the same bird in the pair that has the longer path length across all UMAP renditions? i.e. Is the path length comparison repeatable?



Here, you will find the fourth test:-

4. `Flip Test`

	- In this test, we use the 31 tutored birds from the Alam dataset.
	- For each bird, we have generated their path length in 20 UMAP renditions.
	- We form all possible pairs of birds (= 31 * 30 / 2).
	- For each bird pair, we compare their path lengths across the 20 UMAPs. 
	- We test if the bird in the pair with the longer path length is consistent, i.e. we calculate the probability that the bird in the pair with the longer path length is switched by only changing the UMAP seed.
	- [ ] We want to check the repeatability of the valence of the path length comparison in bird pairs.





The folder `Data` has 1 file which is used as input:-
1. `path_length_df.csv`
	- This has the path length information for each bird.
	- This was computed in previous tests.

The folder `Results` has the relevant results for this test.
	
Specific information  about  these  files is provided in the corresponding README.



Note:

- All the tests were conducted on non-normalised UMAP embeddings.
- The cluster labels are a combination of what they provided + kmeans.

