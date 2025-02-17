## Test #1 RseedRepeatability

In the article `No support for honest signalling of male quality in zebra finch song; Bulla, Sankar, Forstmeier, 2025`, we test the reliability of the path length metric, as described in [Alam et al. (2024, Nature)](https://doi.org/10.1038/s41586-024-07207-4).

We test the path length metric in various contexts, one of which is described in this folder.
We provide here the corresponding scripts and results.



We test this argument:

- Is the path length of a birdsong consistent across different UMAP renditions? i.e. Is the path length metric repeatable?





#### Test description

Here, you will find the description of the test we run to examine the above argument.


	-  In this test, we make 20 UMAP embeddings of the same dataset of 31 tutored birds ("tut.csv").
	-  We change no parameters, except the seed for the random number generator.
	-  In each of the 20 UMAP embeddings, we compute the path length for each birdsong.
	-  This gives 31*20=620 path lengths, 20 per bird.
	-  Separately, in R, we check the repeatability of the path length of a birdsong, across different seeds for the random number generator.



#### Test reproducibility

For reproducing the results,
the python scripts related to this test are in the folder `Scripts`.


#### Test results

The `Results` folder has the corresponding results.


	
Specific information  about  these  files is provided in the corresponding README.

