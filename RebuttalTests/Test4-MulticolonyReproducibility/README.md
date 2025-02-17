## Test #4 Multi-colony Reproducibility

In the article `No support for honest signalling of male quality in zebra finch song; Bulla, Sankar, Forstmeier, 2025`, we test the reliability of the path length metric, as described in [Alam et al. (2024, Nature)](https://doi.org/10.1038/s41586-024-07207-4).

We test the path length metric in various contexts, one of which is described in this folder.
We provide here the corresponding scripts and results.



We test this argument:

- Is the path length of a birdsong consistent across different colonies of birds? i.e. Is the path length metric reproducible?


#### Test description


Here, you will find the description of the test we run to examine the above argument.


	- In this test, we use the 31 tutored birds from Alam et. al ("tut.csv").
	- 1 bird is chosen as the focal bird.
	- 5 non focal birds are chosen from the 30 leftover birds. ( C(30,5) )
	- A UMAP embedding is generated for these 6 birds.
	- We compute the path length of the focal bird in this UMAP.
	- For the same focal bird, we repeat this process 10 times, i.e. choose 5 non focal birds, generate a UMAP embedding and compute path length.
	- This gives 10 path lengths for a given focal bird.
	- Then, we repeat this process for each of the 31 birds as the focal bird.
	- This generates 31*10=310 path lengths, 10 per bird.
	- Separately, in R, we check the reproducibility of the path length of a birdsong, given changing neighbours.




#### Test reproducibility

For reproducing the results,
the python scripts related to this test are in the folder `Scripts`.




#### Test results

The `Results` folder has the corresponding results.


	
Specific information  about  these  files is provided in the corresponding README.

