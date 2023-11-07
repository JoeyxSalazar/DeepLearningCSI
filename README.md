ECE 553/ 653 Neural Networks

# Project 1: Vehicle Positioning

You will design a simple machine learning algorithm for vehicle positioning. Your algorithms will be
responsible for estimating vehicle position using channel state information from the users. Your protocol
will be tested on an emulated unreliable network.

# 1.Requirements

You will write **two** programs: a LoS/NLoS classification program that classifies the signals of the vehicle
according to the channel state information (CSI ), and a vehicle positioning program that estimates the
vehicle position using CSI. It is recommended that your programs are written in python.

For each program, you will propose a machine learning (ML) method (i.e., regression, KNN) and an artificial
neural network (ANN) method.

You have to design your own data preprocessing method, input format, neural network architecture, and
use ML and ANNs for LoS/NLoS signal classification and vehicle positioning.

# 2.Dataset Introduction

This CSI dataset is collected in an underground parking lot of an office building. For data collection, the
vehicle is randomly placed at 476 different locations which are either line -of-sight (LoS) or non -line- of-
sight (NLoS). The scenario layout and information of the 476 locations are shown in the two images above.

The CSI dataset has been divided into a training dataset with 15000 data samples and a validation dataset
with 5000 data samples. Each data sample includes a complex-valued CSI matrix used as input of a model,
and one label vector. The CSI matrix has a dimensionality of 4 × 1632 , where 4 is the number of antennas
of the remote radio unit (RRU), and 1632 is the number of sub-carriers. The label vector has 3 dimensions,
in which the first two dimensions respectively represent the x and y coordinates of the vehicle (relative to
the coordinate of RRU), and the third dimension is a binary LoS/NLoS indicator (0 for LoS, 1 for NLoS).

The two datasets are named as ‘train_dl.pt’ and ‘valid_dl.p t’. To read in those two files, you may need to
install and import the following libraries: torch, torch.utils.data.TensorDataset, torch.utils.data.DataLoader.
There are other aspects that you can explore and report, which are up to you. More comprehensive study
will receive more credits.




