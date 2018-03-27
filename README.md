# SYSU_Graduation_Project
This is my graduation project about unsupervised person re-id

## CNN
The CNN file is the baseline of the model, I finally select ResNet-50 as the base model to extract the features.

## Setup
All of the code is implemented with Keras, Tensorflow(Python).
You can install all of the setting with pip.

## How to run
### 1.Download the datasets(DukeMTMC,CUHK03,Market1501) in the offical website or any other places.
### 2.Create a "train.list" for every dataset with the following format:
  image name                id    
  0001_c2_f0046182.jpg      0    
  0001_c2_f0046183.jpg      0    
  ...                       1    
  0749_c5_f7528193.jpg     750    
  So as to the "test.list" and "query.list", which are for probe and query
### 3.Train the base model(ResNet-50) on the dataset A, such as DukeMTMC, and move the trained model the 'Model' file.
### 4.Let B as the target dataset,such as Market1501, modify A->B in Model/unsupervised.py.