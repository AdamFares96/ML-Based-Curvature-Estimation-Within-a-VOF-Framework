# ML-Based-Curvature-Estimation-Within-a-VOF-Framework

This repository aims at exploring different machine learning approaches to estimate curvature directly from volume fraction. It includes:

#	DataSets.zip
The data sets used to train the model can be found in this file/
DS1: 15000 example, 3x3 stencil
DS2: 50000 example, 3x3 stencil
DS3: 50000 example, 5x5 stencil

# DataGeneration.ipynb
This code was used to generate the well balanced synthetic datasets used. It is based on the procedure detailed in:	
Patel, H. V., Panda, A., Kuipers, J. A. M., & Peters, E. A. J. F. (2019). Computing interface curvature from volume fractions: A machine learning approach. Computers & Fluids, 193, 104263.

# FeedForwardNN.ipynb
This code contains the Fully Connected Neural Network used to "predict curvature. It has three hidden layers, each with 80 neurons. It uses the data generated in "DataGeneration.ipynb" and presented in "DataSets.zip" as input.

#	BinaryClassification.ipynb
This code contains the neural network for binary classification approach to this problem. It generates a volume fraction field and trains a NN given centroids to output volume fractions. The Boundary equations of the neurons in the hidden layer are extracted and in fact represent the curvature.  
