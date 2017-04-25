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
3. Put the content into a folder /capstone-project/data/data folder. Or use your own folder structure and change the path in the notebooks.

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
These are the different models for this project.

### SVM
Specifiy npz-file and run the notebook.
~~~~
capstone-project/notebooks/3.1 Support Vector Machine (SVM).ipynb
~~~~

### K-Nearest
Specifiy npz-file and run the notebook.
~~~~
capstone-project/notebooks/3.2 K-Nearest.ipynb
~~~~

### CNN
I recommend training CNNs on the GPU because it is much faster than on CPU. The CNN_small can be trained with data coming from a npz-file if it is not too big. The CNN - VGG16 and CNN - ResNet50 are designed to load the data in batches from directories, so we have no problem that the data won't fit in memory if we want to train on all images.

### CNN_small
Specifiy npz-file and run the notebook.
~~~~
capstone-project/notebooks/3.3 CNN_small.ipynb
~~~~

### CNN - VGG16
Specify train and test folder in the ImageDataGenerators.
~~~~
capstone-project/notebooks/3.4 CNN - VGG16.ipynb
~~~~
