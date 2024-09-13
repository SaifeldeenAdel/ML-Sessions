# Build a Simple Neural Network for Binary Classification

Binary Classification is a type of machine learning task where the goal is to categorize data into one of two possible classes. In this case, the Breast Cancer dataset involves predicting whether a tumor is benign (non harmful) or malignant (harmful) based on various features.

### Data Loading:

-   Load the [Breast Cancer dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html) from sklearn.datasets.
-   Select any two features from the Breast Cancer dataset (e.g., mean radius and mean texture). Plot the data points using these two features on a 2D scatter plot. Use different colors to represent the two classes (benign and malignant). Will a linear model work with this data?

-   Split the dataset into training and test sets (e.g., 80% training, 20% testing).

### Model Architecture:

-   Build a simple neural network using PyTorch.

-   Think about what layers should your network have? Will it only involve linear layers? Remember activation functions?

Training:

-   Define a loss function (see [BCELoss](https://pytorch.org/docs/stable/generated/torch.nn.BCELoss.html))
-   Use an optimizer like SGD or Adam.
-   Train the model over multiple epochs, adjusting learning rate as needed.
-   Print out loss and accuracy (for accuracy, see [accuracy_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html)) as you go through your epochs.

Evaluation:

-   Evaluate the model on the test set.
-   Report the accuracy see [accuracy_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html) of the model.
-   Plot train and/or loss vs epochs such as below

![img](/02/img/Screenshot%202024-09-13%20190554.png)

## Deliverables:

-   Code: A Python script or notebook with the implementation

-   Visuals in notebook include
    -   Dataset plot
    -   A loss vs. epochs plot

## Resources

[Neural Network Playlist](https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi&ab_channel=3Blue1Brown)

[PyTorch Tutorials (1-12)](https://www.youtube.com/watch?v=EMXfZB8FVUA&list=PLqnslRFeH2UrcDBWF5mfPGpqQDSta6VK4&ab_channel=PatrickLoeber)
