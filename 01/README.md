# Session 1 Assignment

## Intro to ML - Exploring Classification Algorithms and scikit-learn.

#### Objective:

This assignment will test your understanding of classification and regression by guiding you through building simple models using real-world datasets. You'll implement both classification and linear regression, covering topics we discussed in the session.

### Classification using K-Nearest Neighbors (KNN) + 2 other algorithms.

Instructions:

**Dataset:** Use the famous [`iris` dataset](https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html)

This dataset contains 150 samples of iris flowers with four features (sepal length, sepal width, petal length, petal width). Each flower is classified into one of three species: Setosa, Versicolor, or Virginica.

### Task 1:

Build a K-Nearest Neighbors (KNN) classifier to predict the species of the flower based on the features provided.

**Simple walkthrough (not full)**:

-   Load the Iris dataset (look through sklearn docs to find out how)
-   80/20 train/test split.
-   Train a KNN classifier using the training set (see sklearn docs)
-   Make predictions on the test set.

Output:

-   Evaluate the model using accuracy (number of correct predicitons over total test set) and **print the accuracy**
-   **Plot the decision boundary of your model, see the image below.**

![img](/01/img/Screenshot%202024-09-11%20202631.png)

### Task 2:

Repeat the same process using 2 other classification algorithms of your choice.

Research other classification algorithms (examples include Decision tree, Linear SVM, RBF SVM, Naive Bayes) all of which you'll find implementation for on in scikit-learn.

Discuss which alogorithm would you choose and why? (there might not be a right answer, only correct reasoning for your choice).

## Deliverables

-   Code Notebook showing your algorithms and the code used the plot the decision boundaries
-   Algorithm Discussion, which algorithm is the best, etc. Can be in the notebook or a seperate document
