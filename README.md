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
After the data preprocessing, we need to see that dataset again and see some visualization from training data. By this code, one can see the image and label for the training. As the data is labeled with correct output the image will match the label. You can change the index value and the image and label will change with respect to your index value. Matplotlib library has been used to see the image. Using the F-string code format, a title is produced.

## Step 5: Building The Model
In these lines of code, the model is being produced. Using the Sequential model, ANN is being trained for feedforward propagation. With this, the data flows in only one direction. To match this thing, a Flatten layer has been used to convert 2D input (28x28 images) into a 1D array (784-dimensional vector). This is much necessary because the hidden layer (Dense layer) could get a flat input. The Dense layer has 128 neuron in it which is a building block for ANN. The activation function "relu" has been used to add some non-linearity to the model. It is also required because image recognition is a non-linear problem. The final Dense layer is an output layer which has 10 neurons for the 10 digits like 0-9. The activation function is softmax which adds up all the probabilities equal to 1.

## Step 6: Checking the Overall Summary of the Model
This code provides a summary of our model. It shows Total parameters, Trainable parameters, and Non-trainable parameters as output.
### Flatten layer: 
This layer shows that the total pixels of the input image like 28x28 have been converted to 784-dimensional vector. Also, it has no trainable parameters because this is only reshaping the vector and nothing else.
### Dense layer: 
This layer shows that it has 128 neurons in it. Which means that it will produce 128 outputs for each input. Also, it shows params as 100,480 which can be calculated as follows.
784 features connected with 128 neurons====> 784*128 = 100,352
Now add 128 bias values====> 100352+128= 100,480
### Output Layer:
This dense layer is used as the output layer. It has 10 neurons for 10 types of digits like 0-9.
The calculation for params is the same.
128 inputs from the previous layer connected with 10 neurons ====> 128*10 = 1280
now add 10 bias with value to give 1290 as params.

## Step 7: Compiling the model
Here the model is compiled. The compile() function defines how a model will be trained by using the loss function, optimizer, and metrics to evaluate performance. By this loss and accuracy can be easily measured. The Loss as "sparse_categorical_crossentropy" is used for multi-class classification problems where the labels are given as integers. The loss function shows the difference between the probability of a number and the original number. Optimizer is used to update the weights while the model is being trained. Accuracy is being used as metrics which is used to see the performance of the model.

## Step 8: Training the model
The fit() method is used to train the model on the given training dataset. Epochs show how many times the model will be iterated to get the best performance. This number should be chosen by various numbers but keep in mind that the model is not getting overfitted. "Validation_split" shows that 20 percent of the training data will be used for validation purposes.

## Step 9: Model Evaluation with respect to Accuracy
Here the evaluate() method provides the model performance on testing dataset based on trained model. Two things loss and accuracy has been evaluated with the model. Verbose controls the information like how much information would be presented as output to this code. Now we have two outputs like test loss and test accuracy.










