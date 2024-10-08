# Character_Recognition-_using_Tensorflow

## Introduction: 
This report gives the complete details of the processes and the result of the project. Here, a pattern recognition project has been made using the MNIST dataset. This dataset has a huge number of handwritten digits which are to be recognized. A TensorFlow framework using the ANN model has been produced to correctly recognize those digits. The result and the accuracy are well enough to predict the digit pattern in the image form.

## Before Getting Started
You need to check and install some important libraries used for this project. This list has been provided in the "Requirements" file. In the project file, you just need to remove the "#" sign and that library will be installed in your Jupyter notebook. If that library is already installed then you will see the notification as requirements already satisfied. 

## Step 1: Importing Libraries
Once you installed all the required libraries then you need to import them so that these can be used in the programming for various purposes. All four libraries have been imported in this step. Then from the Tensorflow library, Keras, Sequential, and some layers like Dense and Flatten have been imported so that ANN model could be easily built and trained for predictions. 

## Step 2: Loading the MNIST Dataset
In this step, MNIST dataset which is already available in the framework has been imported for digit recognition. The MNIST dataset is a dataset consisting of 70,000 grayscale images of handwritten digits. Each image is 28x28 pixels in size. We are going to use it for our task of digit recognition.

## Step 2.1 to 2.4: Getting familiar with the dataset
In these steps both the training and testing dataset has been checked. For both variables X and Y, their values and shape has been checked. Also how much adat has been used for training and how much for testing? The total dataset has 70,000 images so 60,000 have been used for training the data and 10,000 images would be used for testing purpose.

## Step 3: Data Preprocessing
The overall dataset has not been normalized for better use. In this process, the range has been adjusted for more convergence. For example, the MNIST dataset has a range of 0 to 255 for the original pixel value of each greyscale image. For normalization purposes, we need to have pixel scale values between 0 and 1 so that there should be consistency in the input and the model could be better trained for prediction. That's why each value has been divided by 255 in both training and testing datasets.

## Step 4: Data Visualization
After the data preprocessing, we need to see that dataset again and see some visualization from training data. By this code, one can see the image and label for the training. As the data is labeled with correct output the image will match the label. You cane change the index value and the image and label will change with respect to your index value.










