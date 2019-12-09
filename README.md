# Generative Adversarial Networks

>"the coolest idea in machine learning in the last twenty years." - Yann LeCun

## Introduction
**Generative adversarial networks**(GANs) are a recent innovation(2014) in machine learning invented by Ian Goodfellow and his colleagues. Given a training set, a neural network will learn to generate new data with the same statistics as the training set.
For example, GANs can use a training set of photographs of human faces to create images of human faces. These generated images don't belong to any real person.

![alt text](https://github.com/pejner/keras-gan/blob/master/images/gan_faces.png "Generated faces from GAN created by NVIDIA")

### How do GANs work?
GANs consist of two neural networks that contest with each other. The generative network generates plausible candidates while the discriminative network evaluates candidates by distinguishing the generator's fake data from real data.

At the beginning of training, the generator will produce data that is obviously fake and the discriminator quickly learns to tell that it is fake data:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/bad_gan.svg "Bad GAN example")

As training continues, the generator will continue to get closer to producing output that can fool the discriminator:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/ok_gan.svg "Decent GAN example")

Eventually, if the generator training goes well, the generator will produce data which is difficult to distinguish as fake or real. The discriminator gets worse at telling the differences and accuracy decreases:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/good_gan.svg "Good GAN example")

Picture of the whole system:
![alt text](https://github.com/pejner/keras-gan/blob/master/images/gan_diagram.svg "GAN overview")

## GAN Anatomy

### Discriminator
The discriminator in a GAN is a classifier. The discriminator tries to distinguish real data from the data created by the generator.

#### Discriminator Training
During discriminator training, the generator does not train. The weights for the generator remain constant while it produces images for the discriminator to train on.

The data used for training the discriminator comes from two sources:

- **Real Data** are considered positive instances during training.
- **Fake Data** are considered negative instances during training.

If the discriminator misclassifies real instance as fake or fake data as real, the discriminator loss penelizes the discriminator. Discriminator will use the discriminator loss to update its weights through backpropagation.

### Generator

## Applications

### Science

### Fashion, art, advertising

### Video games

### Concerns of possible malicious applications

## Common Problems

### Vanishing Gradients

### Failure to Converge

### Mode Collapse



## Contributors
Prad Ejner
Dan Mohler
Jordan Winkler