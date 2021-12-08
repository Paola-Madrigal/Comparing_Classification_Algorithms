# Comparing Classification Algorithms
There are a lot of different methods to approach a Classification issue. The intent of this article is to compare between 5 different Classification models. We will be using a simple dataset with two features (Age, Interest) and one target (Success). The dataset was obtained from Kaggle: https://www.kaggle.com/sveneschlbeck/beginners-classification-dataset

Resources:
* Dataset: https://github.com/Paola-Madrigal/Comparing_Classification_Algorithms/blob/main/classification.csv
* Script: https://github.com/Paola-Madrigal/Comparing_Classification_Algorithms/blob/main/comparing-different-algorithms.ipynb

The 5 Classification algorithms we will be using are the following:

1. Logistic Regression
2. Random Forest
3. Support Vector Machine
4. K-Nearest Neighbors
5. Neural Network

First, we will start with a visualization of each feature vs the target:

![image](https://user-images.githubusercontent.com/93732824/145284508-3dedf39b-a933-45d3-9657-e8c8128d328a.png)

This help us visualize that we are dealing with a classification issue, since Success only takes values of 0 or 1. We can also see that Interest seems to have a higher influence on wether Success will be achieved or not. Age seems to have a small influence as well, but not as strong as Interest.

## 1. Logistic Regression
Logistic Regression is one of the simplest, most intuitive models we can use. It basically builds a sigmoid curve to obtain the probability of success based on the feature value:

<p align="center">
<img width="460" height="300" src="https://user-images.githubusercontent.com/93732824/145291451-0fe7a062-49ce-4333-b37d-69c11005c434.png">
</p>

When applying Logistic Regression to our data, we get the following weights:
* Age Weight: 0.5457
* Interest Weight: 2.8298

This confirms that Interest has indeed a higher influence on Success than Age.

Let's review the accuracy we get:
* Train accuracy: 0.8734 
* Test accuracy: 0.9167

## 2. Random Forest
Random Forest is based on several Decision Trees. Each Decision Tree comes up with an output, and the final output will be defined by the majority result of the Decision Trees:

![image](https://user-images.githubusercontent.com/93732824/145289999-d80fd1ac-9b20-4850-919c-272276621c8a.png)

With this algorithm, we can also retrieve the importance of each feature, and we can once again see that Interest has a higher influence:
* Age importance: 0.287221
* Interest importance: 0.712779

Let's review the accuracy we get:
* Train accuracy: 1.0 
* Test accuracy: 0.9833

## 3. Support Vector Machine
Support Vector Machine uses a hyperplane to generate the model. The optimal hyperplane is the one that maximizes the gap or margin between the two classes. The most simple model uses a linear kernel function. However, we can use different kernel functions in order to improve accuracy for more complex data:

<p align="center">
<img width="460" height="300" src="https://user-images.githubusercontent.com/93732824/145304025-a063c960-d73c-4644-8b4a-9d0b7804a348.png">
</p>

Let's review the accuracy we get:
* Train accuracy: 0.9494 
* Test accuracy: 0.9833

## 4. K-Nearest Neighbors
