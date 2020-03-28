# Brain MRI Generator
A generative adversarial network(GAN) using the Keras library to train a neural network to generate brain MRI’s with the same statistics as MRI’s from a training set.

## Dataset
ArtUK was used for initial evaluation of model  
brain_tumor_mri_dataset contains images used for testing of various sizes  

## Models
art-gan.py was used to generate images from the ArtUK dataset  
brain-gan.py was used to generate images from mri-dataset with evaluation every 100 epochs  
brain-gan-parameter-search.py was used to generate images with varying parameters, with output only at the end 


