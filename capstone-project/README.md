# Image Classification - Caltech256

## Dependencies:

- Anaconda:
https://docs.continuum.io/anaconda/install<br>

- Tensorflow:
https://www.tensorflow.org/install/<br>

~~~~
pip install environment.yml
~~~~

## Instructions for use:
1. Clone the repository
~~~~
git clone https://github.com/fses91/data-science-intensive.git
~~~~
2. Download the dataset
http://www.vision.caltech.edu/Image_Datasets/Caltech256/256_ObjectCategories.tar
3. Put the content into the data/data folder.

## Prepare data for sklearn
If we want to use the data for sklearn we need numpy arrays. The "2. Data Preparation.ipynb" notebooks creates npz-files with a specified amount of classes. Later we can load the data from these files in a simple way.
~~~~
capstone-project/notebooks/2. Data Preparation.ipynb
~~~~

## Prepare data for tensorflow
If we want to use the data for keras we can also load the npz-files and train. But the whole data would not fit in memory.
The script "2.1 Data Preparation - Split-Train-Test.ipynb" splits the data in a specified folder into two seperate folders for train and test. The size of the train - test split can be specified in the script. 
~~~~
capstone-project/notebooks/2.1 Data Preparation - Split-Train-Test.ipynb
~~~~

## Models
The scripts for the SVM and K-Nearest are very easy. Just specify the npz-file you want to load and the script does everything else for you. The script for the CNN is also very easy just specify the train and test folder in the generator and run the script. 


### SVM
~~~~
capstone-project/notebooks/3.1 Support Vector Machine (SVM).ipynb
~~~~

### K-Nearest
~~~~
capstone-project/notebooks/3.2 K-Nearest.ipynb
~~~~

### CNN
I recommend training CNNs on the GPU because it is much faster than on CPU.
