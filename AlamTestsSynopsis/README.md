## Testing global distances between UMAP clusters

We test two arguments:

1. Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable.
2. Distances b/w any two clusters are dependent not just on the properties of the samples of these two clusters, but also on the other samples in the dataset. Hence, the pairwise distances are a relative measure, not an absolute one, at best.

Here, you will find the three corresponding tests:-

1. `Split Comparison Test`

	- In this test, we use 31 tutored birds from the Alam dataset.
	- 1 bird is chosen as the focal bird.
	- The 30 non focal birds are randomly split into two, with 15 birds each.
	- This makes 2 subsets of 16 birds each, both containing the focal bird.
	- We generate the UMAP embeddings for these 2 subsets with the given focal bird.
	- We compute the path length of the focal bird in these 2 UMAPs.
	- Then, we repeat this for each of the 31 birds.
	- This generates 31*2=62 path lengths, 2 each per bird.
	- [ ] We want to check the repeatability of the path length of a bird, given different neighbours.

2. `Combination Test`

	- In this test, we use 31 tutored birds from the Alam dataset.
	- 1 bird is chosen as the focal bird.
	- 5 non focal birds are chosen from the 30 leftover birds. ( C(30,5) )
	- The UMAP embedding is generated for these 6 birds.
	- We compute the path length of the focal bird in this UMAP.
	- For the same focal bird, we repeat this process 10 times, i.e. choose 5 non focal birds, umap, path length.
	- This gives 10 path lengths for this focal bird.
	- Then, we repeat this for each of the 31 birds.
	- This generates 31*10=310 path lengths, 10 per bird.
	- [ ] We want to check the repeatability of the path length of a bird, given changing neighbours.

3. `Rseed Test`

	-  In this test, we make 20 UMAP embeddings of the same dataset of 31 tutored birds.
	-  We change no parameters, except the seed for the random number generator. 
	
	- a. `Path length`
		- In each of the UMAP embeddings, we compute the path length for each bird.
		- This gives 31*20=620 path lengths, 20 per bird.
		- [ ] We want to check the repeatability of the path length of a bird, across diff seeds for the random number generator.
	- b. `Pairwise distance`
		-  In each of the UMAP embeddings, we compute the euclidean distances b/w each pair of syllable clusters.
		- With 150 syllable clusters, this makes ( 150 x 149 ) / 2  = 11175 pairs.
		- With 20 UMAPs, this gives 11175 * 20 = 223500 pairwise distances in total.
		- [ ] We want to check the repeatability of the pairwise distance b/w 2 given clusters, across diff seeds for the random number generator.



Here, you will find the folders related to these tests:-

1. `Test1-SplitComparisonTest`

2. `Test2-CombinationTest`

3. `Test3-RseedTest`

	a. `Test3a-PathLength`
	
	b. `Test3b-PairwiseDistance`



Each test folder has 3 files:-
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



To do:

- [ ] Compute repeatability metrics.
- [ ] Recompute with normalised UMAP embeddings.
- [ ] Filter out stable cluster labels, and only use those to compute repeatability.
- [ ] Add samples for test #1.