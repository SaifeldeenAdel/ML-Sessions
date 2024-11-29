# Building an Image Classification Model Using PyTorch

## Aim

In this assignment, you will design, train, and evaluate a convolutional neural network (CNN) from scratch to perform an image classification task. The goal is to gain hands-on experience with data preparation, model design, training, and evaluation using PyTorch

## Dataset:

[Caltech 101](https://www.kaggle.com/datasets/imbikramsaha/caltech-101)
The Caltech 101 Dataset contains images from 101 object categories (e.g., airplanes, faces, flowers) with varying numbers of samples per class (40-800)

**How to load dataset into google colab?**

-   Download the dataset as zip - 137 MB
-   Upload it to google drive
-   Mount your drive in your colab notebook
-   Access zip file a path like `/content/drive/dataset`
-   Look into how to unzip files in colab, unzip the file and you'll have access to all the folders

Find more details [here](https://www.geeksforgeeks.org/how-to-load-a-dataset-from-the-google-drive-to-google-colab/)

## Assignment

### 1. Data Preparation

The Caltech 101 dataset is structured with subfolders, where each subfolder contains images corresponding to a specific class label. For example, the folder `airplanes/` contains all images of airplanes, and `faces/` contains all images of faces. You will need to organize and preprocess the dataset to create a training and testing split.

Details:

-   Create some structure that holds all image paths with their corresponding label `[("path1", label), ("path2", label)]` so that you can read the image only when needed (later in the `Dataset` class)

-   Split the structure to create a train, test split.

-   Create a custom Pytorch [Dataset](https://pytorch.org/tutorials/beginner/basics/data_tutorial.html#creating-a-custom-dataset-for-your-files) which takes the structure which contains the paths and label (whether train or test) to load your images and labels.

-   Implement the `__getitem__` and `__len__` classes for your dataset to read the images and apply the transform below.

-   Apply a Resize transform in your dataset so that when any image is read, its resized to 128x128x3 (or 3x128x128) (see the transforms applied [here](https://pytorch.org/tutorials/beginner/data_loading_tutorial.html#dataset-class))

-   Create a Pytorch [Dataloader](https://pytorch.org/tutorials/beginner/basics/data_tutorial.html#preparing-your-data-for-training-with-dataloaders) object to load batches of your images

### 2. CNN Model Creation & Training

-   Build a Convolutional Neural Network (CNN) from scratch for image classification. Your CNN should take the 128x128 images as input and output probabilities for each class.

-   Think of your layer dimensions (ex, how many neurons in the last layer?)

-   Train the model using a suitable loss function (e.g., [cross-entropy loss](https://pytorch.org/docs/stable/generated/torch.nn.CrossEntropyLoss.html) for multi-class classification).

-   Use the [Adam](https://pytorch.org/docs/stable/generated/torch.optim.Adam.html) optimizer

-   Experiment with hyperparameters, including batch size, learning rate, and number of epochs.

-   Plot **Loss** and **Accuracy** at the end of training (by storing loss and accuracy values after every epoch)

[Pytorch training loop example code, training a classifier](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html)

### 3. Test Set evaluation

-   Run your final model on the test set and report the loss and accuracy of your model.

Visualization - Optional:

-   Display images from your test set along with their predictions and true label to visualize model results.

## Deliverables

-   Google Colab Notebook:
-   The complete code for loading the dataset, defining the model, training, and evaluating.
-   Well-documented with comments and explanations for every step.

Resources

-   [Datasets - Dataloaders](https://www.youtube.com/watch?v=PXOzkkB5eH0&t=605s&ab_channel=PatrickLoeber)
-   [Dataset Transforms](https://www.youtube.com/watch?v=X_QOZEko5uE&ab_channel=PatrickLoeber)
-   [PyTorch Playlist](https://www.youtube.com/watch?v=EMXfZB8FVUA&list=PLqnslRFeH2UrcDBWF5mfPGpqQDSta6VK4&ab_channel=PatrickLoeber)
-   [Full Workflow tutorial - (Very useful for understanding datasets, training loop, etc. He doesn't build the model from scratch so don't copy his code ofcourse.)](https://www.youtube.com/watch?v=tHL5STNJKag&ab_channel=RobMulla)
