[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"


## Project Overview

Given an image of a food dish, algorithm will identify an estimate of the dish nutrition class.

![Sample Output][image1]


## Project Instructions

### Instructions

1. Clone the repository and navigate to the downloaded folder.

	```
		git clone https://github.com/aleksas/food_nutrition_classifier_tf.git
		cd food_nutrition_classifier
	```
2. Download the meta-data and image database and place those in the the same directory as this notebook.
3. Install [Miniconda](https://conda.io/miniconda.html) and create an environment from appropriate yml file located in environmens folder.  

	For __Mac/OSX__:
	```
		conda env create -f requirements/dl_env_mac.yml
		source activate recipes
	```

	For __Linux__:
	```
		conda env create -f requirements/dl_env_linux.yml
		source activate recipes
	```

6. Open the notebook and follow the instructions.

	```
		jupyter notebook Transfer_Learning_Solution.ipynb
	```
