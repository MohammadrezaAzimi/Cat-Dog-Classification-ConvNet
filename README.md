# Cat-Dog-Classification-ConvNet

# Project description: 
In this project, there are 4000 labeled images as cat and dog. The set is divided into training, validation and test sets of 1000, 500 and 500 examples of each class, respectively.

# Implementation: 
The project is written in Python language using TensorFlow library as backend and Keras package.

# Data preprocessing: 
The images are mapped from JPEG to RGB of size (150,150) and then normalized such that the value of each pixel belongs to [0,1]. The scaling is done using Keras code ImageDataGenerator(rescale=1./255). Also, resizing the images is done using the code .flow_from_directory(train_dir,target_size=(150, 150),batch_size=20,class_mode='binary').

# Network model: 
Four convolutional layers each of them followed by a maxpooling layer and then the result is converted to a vector and fed to a fully connected layer of 512 hidden units with ReLU activations and the output layer has a sigmoid activation.

Since the training set is comprised of 2000 data points, generating batch sizes of 20 samples using generator object requires setting the number of steps per each epoch equal to 100. 

# Modification: 
To increase the accuracy, data augmentation is used to obtain more training data. 

