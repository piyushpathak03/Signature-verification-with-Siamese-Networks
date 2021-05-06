# Signature verification system using Siamese networks
![Siamese Network](https://cdn-images-1.medium.com/max/800/1*LwOBbwGXMZUy6OzkFAPTzw.png)

# Siamese Networks
A Siamese Neural Network is a class of neural network architectures that contain two or more identical subnetworks. ‘identical’ here means, they have the same configuration with the same parameters and weights. Parameter updating is mirrored across both sub-networks. It is used to find the similarity of the inputs by comparing its feature vectors, so these networks are used in many applications
Traditionally, a neural network learns to predict multiple classes. This poses a problem when we need to add/remove new classes to the data. In this case, we have to update the neural network and retrain it on the whole dataset. Also, deep neural networks need a large volume of data to train on. SNNs, on the other hand, learn a similarity function. Thus, we can train it to see if the two images are the same (which we will do here). This enables us to classify new classes of data without training the network again.

## Pros and Cons of Siamese Networks:
### The main advantages of Siamese Networks are,
1. More Robust to class Imbalance: With the aid of One-shot learning, given a few images per class is sufficient for Siamese Networks to recognize those images in the future
2. Nice to an ensemble with the best classifier: Given that its learning mechanism is somewhat different from Classification, simple averaging of it with a Classifier can do much better than average 2 correlated Supervised models (e.g. GBM & RF classifier)
3. Learning from Semantic Similarity: Siamese focuses on learning embeddings (in the deeper layer) that place the same classes/concepts close together. Hence, can learn semantic similarity.

### The downsides of the Siamese Networks can be,
1. Needs more training time than normal networks: Since Siamese Networks involves quadratic pairs to learn from (to see all information available) it is slower than normal classification type of learning(pointwise learning)
2. Doesn’t output probabilities: Since training involves pairwise learning, it won’t output the probabilities of the prediction, but the distance from each class

## Objective
> The objective of the project is to create a deep learning network which classifies signatures as genuine and forgery using Siamese networks with the help of this [paper](https://arxiv.org/abs/1707.02131)
## Dataset
> The dataset that I have used is ICDAR 2011 dataset, which can be downloaded from [here](https://drive.google.com/drive/folders/1hFljH9AKhxxIqH-3fj72mCMA6Xh3Vv0m)

## Loss functions used in Siamese Networks:
Since training of Siamese networks involves pairwise learning usual, Cross entropy loss cannot be used in this case, mainly two loss functions are mainly used in training these Siamese networks, they are
#### Triplet loss is a loss function where a baseline (anchor) input is compared to a positive (truthy) input and a negative (falsy) input. The distance from the baseline (anchor) input to the positive (truthy) input is minimized, and the distance from the baseline (anchor) input to the negative (falsy) input is maximized.
In the above equation, alpha is a margin term used to “stretch” the distance differences between similar and dissimilar pairs in the triplet, fa, fa, fn are the feature embeddings for the anchor, positive and negative images.
During the training process, an image triplet (anchor image, negative image, positive image)(anchor image, negative image, positive image) is fed into the model as a single sample. The idea behind this is that distance between the anchor and positive images should be smaller than that between the anchor and negative images.
#### Contrastive Loss: is a popular loss function used highly nowadays, It is a distance-based loss as opposed to more conventional error-prediction losses. This loss is used to learn embeddings in which two similar points have a low Euclidean distance and two dissimilar points have a large Euclidean distance.



## Results
![](https://cdn-images-1.medium.com/max/800/1*Vk-I-LdrnBDPNYx1bexRMg.png)
![](https://cdn-images-1.medium.com/max/800/1*NxI-UdSnLtX-SWFAYOZ7kQ.png)

## About me

**Piyush Pathak**

[**PORTFOLIO**](https://anirudhrapathak3.wixsite.com/piyush)

[**GITHUB**](https://github.com/piyushpathak03)

[**BLOG**](https://medium.com/@piyushpathak03)


# 📫 Follw me: 

[![Linkedin Badge](https://img.shields.io/badge/-PiyushPathak-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/piyushpathak03/)](https://www.linkedin.com/in/piyushpathak03/)

<p  align="right"><img height="100" src = "https://media.giphy.com/media/l3URDstnIjBNY7rwLB/giphy.gif"></p>

