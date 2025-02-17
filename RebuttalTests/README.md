# README

In the [current](https://github.com/ymir-k/UMAP_test/tree/main/RebuttalTests) repository and [rebuttal_alam_2024](https://github.com/MartinBulla/rebuttal_alam_2024), we provide supporting information for the article: `No support for honest signalling of male quality in zebra finch song; Bulla, Sankar, Forstmeier, 2025`.


In the article, we test the reliability of the path length metric, as described in [Alam et al. (2024, Nature)](https://doi.org/10.1038/s41586-024-07207-4).

To do so, we generate the path lengths in several contexts in this repository and compute the corresponding repeatability in [rebuttal_alam_2024](https://github.com/MartinBulla/rebuttal_alam_2024).


We introduce the different contexts below. Specific information is provided in the corresponding directories.


### Test descriptions

1. [Test1-RseedRepeatability](https://github.com/ymir-k/UMAP_test/tree/main/RebuttalTests/Test1-RseedRepeatability/): This test generates 20 UMAP embeddings of the entire dataset of 31 tutored birds. It changes no parameters, except the seed for the random number generator. It tests the repeatability of the path length for each bird, across multiple UMAP renditions. The results of this test is presented in the manuscript.

2. [Test2-Misclassification](https://github.com/ymir-k/UMAP_test/tree/main/RebuttalTests/Test2-Misclassification): This test takes all pairs of birdsongs and checks how consistently the same song has the longer path length in a  given pair. It tests if one bird in a pair can be reliably labelled as the one with the relatively longer path. The results of this test is presented in the manuscript.

3. [Test3-SplitReproducibility](https://github.com/ymir-k/UMAP_test/tree/main/RebuttalTests/Test3-SplitReproducibility): This test takes one focal bird, puts it in two sets of 15 different birds, and tests the reproducibility of its song path length, given different accompanying birds. The results of this test is presented in the response letter to the reviewers.

4. [Test4-MulticolonyReproducibility](https://github.com/ymir-k/UMAP_test/tree/main/RebuttalTests/Test4-MulticolonyReproducibility): This test takes one focal bird, puts it in 10 sets of 5 non-focal birds, and tests the reproducibility of its song path length, given different colony of birds. The results of this test is presented in the response letter to the reviewers.
 




#### Test input data


Each test is run using the input dataset provided by [Alam et al. (2024, Nature)](https://doi.org/10.1038/s41586-024-07207-4).

Their dataset provides songs sung by 31 normally reared birds (or tutored) and 18 birds reared without a male tutor (or untutored).

Three input files are required to run the scripts:-

1. [tut.csv](https://dataverse.tdl.org/file.xhtml?persistentId=doi:10.18738/T8/WBQM4I/Q92O9A&version=5.0): The source data file for the songs of the 31 tutored birds.

		+ In this sheet, each row represents one sample syllable.
		+ Column `file_name` has the name of the file with the recording of this syllable. This `file_name` also contains information about the bird name and timestamp.
		+ Column `cluster` provides the label of the syllable cluster this sample syllable belongs to.
		+ Columns `0-2351` provides the RGB value for each pixel in a PIL image of the syllable spectrogram. The coefficients of spectrograms were composed of 28 × 28 time (x axis) and frequency ( y axis) components and the intensity of each pixel was measured from 0 to 255 in the red, green and blue channels (= 28 x 28 x 3).
		+ Columns `file_name` and `cluster` will be used together to derive the number of syllables per bird.
	
2. [iso.csv](https://doi.org/10.18738/T8/WBQM4I/DFA8JM): The source data file for the songs of the 18 untutored birds.

		+ In this sheet, each row represents one sample syllable.
		+ Column `file_name` has the name of the file with the recording of this syllable. This `file_name` also contains information about the bird name and timestamp.
		+ Column `cluster` provides the label of the syllable cluster this sample syllable belongs to.
		+ Columns `0-2351` provides the RGB value for each pixel in a PIL image of the syllable spectrogram. The coefficients of spectrograms were composed of 28 × 28 time (x axis) and frequency ( y axis) components and the intensity of each pixel was measured from 0 to 255 in the red, green and blue channels (= 28 x 28 x 3).
		+ Columns `file_name` and `cluster` will be used together to derive the number of syllables per bird.









#### Test reproducibility

For reproducing the results, the python scripts related to the generation of UMAPs and path lengths are in the folder `Scripts` in each test directory.

The environment description is provided in `requirements.txt`.


The R scripts to compute the repeatability values for each test is provided in the repository  [rebuttal_alam_2024](https://github.com/MartinBulla/rebuttal_alam_2024).




#### Test results


In each test directory, the `Results` folder has the corresponding results.

