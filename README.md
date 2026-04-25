# InsigniaNet: Deep Learning for Military Ribbon Bar Classification

### Introduction

InsigniaNet is an application designed to identify Polish Army ribbon bars from images using Convolutional Neural Networks (CNNs). The model was trained on ribbon bar photographs collected from the internet, as well as images taken from Polish Army uniforms. To improve prediction quality on new images, a dropout layer (`keras.layers.Dropout`) was applied as a regularization technique to prevent overfitting on the training data. The application is capable of recognizing even darkened or slightly faded ribbon bars, achieving an accuracy of approximately 95%.

### How the Application Works

The application was implemented in a Jupyter Notebook environment and is available in Google Colab. The order of code execution is important.

First, the entire `military_ribbon_dataset` directory structure must be imported from GitHub — this is handled by the first code block. The images contained in this directory are used as training data for the model. This code block can be executed multiple times; each time, the `military_ribbon_dataset` folder in Colab will be overwritten.

Next, the second code block should be executed. It builds and trains the model using the input data while also validating the dataset.

The final step is to add a new image to the `military_ribbon_dataset` folder for identification. By default, the image should be saved as `test.png`, although this can be changed in the `img_path` variable. It is important that the photo contains only a single ribbon bar — the model will perform the prediction and indicate the probability of assigning it to a specific class.
