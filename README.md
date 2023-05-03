# Detecting Pneumonia in X-rays Using Image Classification Deep Neural Network

**Author:** Grant Edwards

## Overview

We are looking for a new way to help diagnose pneumonia in pediatric patients by using a deep neural network to automatically detect positive cases of pneumonia.

Pneumonia is a lung infection affecting the alveoli (air sacs located within the lungs).

X-rays can be used to detect and diagnose pneumonia in the lungs by exposing infiltrates (that appear as spots in the lungs) that can help identify infections. Diagnosing pneumonia can be difficult, even for physicians who are trained to identify and diagnose pneumonia, especially in early stages when the alveoli are not fully inflamed. Being able to have a trained image categorization neural network to identify and diagnose cases of pneumonia, in addendum to a doctor, can help reduce incorrect diagnosis.

***

## Business Problem

Goal: Build a image categorizer to detect pneumonia in x-rays
Detecting pneumonia in x-rays can be difficult
Incorrect diagnosis can lead to major health issues
Takes up physicians time

***

## Data

The x-ray images used were from kaggle: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

The images that we will be using to build a deep neural network are x-rays from pediatric patients that are broken into two classes of positive and negative for pneumonia. The images are also split into three groups for training, validation, and testing. The training x-rays will be used to train the model, validation will be used to validate the model as it trains through epochs. Testing x-rays will be used to see how the DNN performs on new images to simulate a real world trial. 

![graph1](./images/Pneumonia-negative.png)

Image1: Negative for Pneumonia


![graph2](./images/Pneumonia-positive.png)

Image2: Positive for Pneumonia


X-rays can be tricky to diagnose when not looking at something obvious like a broken bone, but pneumonia being a viral or bacterial infection causes inflammation in the respiratory organs (lungs). While there is going to be variability in the images as seen above, we can make out some distinctions such as increase distortion and spots in the lungs that can indicate pneumonia.
***

## Methods

To start we checked the x-ray images, as well as the grouping. We found that the provided validation set had only 16 images, so the training set was split (70/30 training, validation respectively). This gave a large enough validation set to be useful. 
Next the ImageDataGenerator was set for the training, validation and testing sets, and models were built using different layers, depth and levels of complexity to try and find a strong model. 


***

## Results


![graph3](./images/linear-model.png)
***

For the linear regression model that we started with, we observed the following:

Precision Score: 0.4706

Recall Score: 0.1333

Accuracy Score: 0.8537

F1-Score: 0.2078

Mean Cross Validation: 0.6547


***

## Conclusions


***

## For More Information

Please review our full analysis in [our Jupyter Notebook](./X-Ray-Pneumonia.ipynb) or our [presentation](./X-Ray-Pneumonia-Presentation.pdf).

For any additional questions, please contact **Grant Edwards, grantedwards11@gmail.com**

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── X-Ray-Pneumonia.ipynb               <- Narrative documentation of analysis in Jupyter notebook
├── X-Ray-Pneumonia-Presentation.pdf    <- PDF version of project presentation
├── Data                                <- Both sourced externally and generated from code
└── images                              <- Generated from code
```
