# Image_Segmentation
Deep Learning Project on Semantic Image Segmentation

Find full report and demo under "presentation". 

## Brief Intro

Image segmentation refers to the task of learning a “mask” for an input image. The mask is apixel-wise classification mask, such that every pixel in the picture is predicted to be part of a singlecategory.

![title](notebook_pics/img_seg2.png)

Above we can see two different types of segmentation: instance and semantic. Instance segmentationtasks aim to not only label each object, but also differentiate between objects of the same class.Semantic segmentation only aims to label objects and non-objects/background. For this project, Iwill be focusing on a semantic segmentation problem.

## Approach

Semantic segmentation represents a new challenge in terms of model construction. This problemdiffers significantly from previously seen simple classification problems. In a simple classificationproblem, we only assign one label to each image (i.e. cat or dog). However, in semantic segmentation,we could have any number of object classes present together in the same photo. So how dowe construct a deep learning model with a variable number of labels for each picture?

In order to properly represent a multi-class image, we will rely heavily on one-hot encodings andsparse matrices. In the example below, we can see that the image contains five different classes ofobjects. Therefore, every pixel in the image receives a label according to the class it belongs. 

![title](notebook_pics/one_hot.png)