## Testing global distances between UMAP clusters

We test two arguments:

1. Different UMAP embeddings of the same dataset, will place the clusters in a different location each time. Hence, the distances b/w clusters in a UMAP space is not repeatable.
2. Distances b/w any two clusters are dependent not just on the properties of these two clusters, but also of the other clusters. Hence, the pairwise distances are a relative measure, not an absolute one, at best.

Here, you will find the two corresponding tests:-

1. No Exclusion
	-  In this test, we make multiple UMAP embeddings of the same dataset.
	-  We change no parameters, except the seed for the random number generator. 
	-  We compute the euclidean distances b/w each pair of digit clusters in each of the UMAP embeddings.
	
2. Exclusion
	- In this test, we make one UMAP embedding per combination of digits.
	- We don't change any parameter, only the input dataset of digits.
	- We compute the euclidean distances b/w each pair of digit clusters in each of the UMAP embeddings.



In this folder, you will find the files related to these tests.

It contains three folders:-

1. Scripts
	- Here, you will find the python scripts to run the test. Feel free to rerun and test them.
	- `Environment/requirements.txt`: This folder gives you the requirements to set up your conda environment
	- `test_umap_no_exclusion.ipynb`: A jupyter notebook for the first test 
	- `test_umap_exclusion.ipynb`: A jupyter notebook for the second test

2. Notebooks
	- In case you don't want to run the python scripts, here are the html or pdf versions of the executed notebook. If it's not clearly commented, let me know.
	- `test_umap_no_exclusion.html`
	- `test_umap_no_exclusion.pdf`
	- `test_umap_exclusion.html`
	- `test_umap_exclusion.pdf`
	
3. Figures/wo1_digits
	- These contain the results of the two tests.
	- `no_exclusion`:
		- `distance_dataframe.csv`: The pairwise distances calculated in every UMAP embedding are stored here for human readable access
		- `distance_matrix.npy`: The pairwise distances calculated in every UMAP embedding are stored here for python access
		- `pairwise_cluster_distances_kmlabel.png`: Result of test 1. The figure is captioned in the notebook.
		- `UMAP_n.png`: Plot for the nth UMAP embedding

	- `exclusion`:
		- `combo_dataframe.csv`: The pairwise distances calculated in every UMAP embedding are stored here. It includes the combo, the cluster centre and the distance matrix.
		- `distance_dataframe.csv`: The pairwise distances calculated in every UMAP embedding are stored here. It's the same as above, just formatted differently for hopefully easier access. It includes the combo, the test pair and the distance.
		- `pairwise_distances_across_combos.png`: Result of test 2. The x axis shows the test pairs. The figure is captioned in the notebook.
		- `pairwise_distances_across_pairs.png`: Result of test 2. The x axis shows the combination. The figure is captioned in the notebook.
		- `UMAPs`: The UMAP plots for each combination of digits

Options:

- If you want to use HDBscan, instead of Kmeans for clustering, just uncomment line 36.


Note:

- All the tests were conducted on the MNIST dataset. The digit 1 was excluded as it formed two separate clusters.
- In test 2, the clustering is faulty at times.

To do:

- [ ] Fix the faulty clustering in test 2. Can perhaps be done by using the flat HDBscan algorithm. To be tested.
- [ ] Implement shortest distance b/w more than 2 clusters.
- [ ] Redo test with their ZF song dataset.
