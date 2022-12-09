# Feature Matching in GANs
##### Amil Dravid, Soroush Shahi -- Northwestern University CS496: Deep Generative Models by Bryan Pardo
### Introduction/Motivation

The performance of deep learning in vision tasks such as image classification and generation has reached new heights in the past decade. However, the internal mechanics of these models remains an open problem. Visualizing and understanding deep neural nets can assist in the development of better models and new insights. To this end, 
one interesting pattern to look at is the similar learned representaions in generative adverserial networks (GANs). Finidng similar representaion will further help to remove duplicate representaitons from a network and reduce the network size resulting in more efficient networks. In this work, we propose a method to find the similar units (i.e, chaneels) in DCGANs by calcualting a similarity score table. 

### Method
We took two identical DCGANs and initialized them with random weights from two different seeds and we call them GAN A and GAN B. This ensures that the two architectures start the training process from different points. We let these two GANs trained with FashionMNISt dataset until convergence. All hyper-parameters are kept the same between the two training process. After training is complete, we unroll both of the networks and compare each feature map from GAN A to each feature map of GAN B and calcualte a similarity score (between 0 and 1). Then we create a similarity score table. The whole process is shown in figure X.

![alt text](assets/method.gif)

