# Convolutinal Neural Network/CIFAR10

Dataset Description ([HERE](https://www.cs.toronto.edu/~kriz/cifar.html)):

General

The dataset contains 10 classes. The class labels can be found in the ‘classes.names’ file. These labels are in exact order as the dataset label id found in the data batches.

Loading

There are 5 batches of data each containing 10000 images. The batches can be loaded with the pickle module in Python. But the option encoding='bytes' needs to be provided. Example:

with open(file, 'rb') as batch_file:
    	data = pickle.load(batch_file, encoding='bytes')

It will return a dictionary object. The core data can be accessed with ‘data’ & ‘labels’ keys. But keep in mind they are in Bytes Literals.

The label ids will correspond to the class labels in order as explained earlier and are self-explanatory.

[IMPORTANT]
The array of the images inside the data is a 10000 x 3072 shaped numpy array. Each row of the array stores one 32 x 32 RGB image. The first 1024 entries contain the Red channel values, the next 1024 the Green, and the final 1024 the Blue. The image is stored in row-major order, so that the first 32 entries of the array are the red channel values of the first row of the image.

Problem 0:
Prepare a smart method to convert the stored image array into a standard library (open-cv, matplotlib etc.) interpretable format.

Problem 1:
Prepare an Image Classifier that can successfully predict the class labels of the images in context.
