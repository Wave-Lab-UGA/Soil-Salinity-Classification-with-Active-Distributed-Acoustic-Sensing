# Soil-Salinity-Classification-with-Active-Distributed-Acoustic-Sensing

## Introduction
Data acquired from a Distributed Acoustic Sensor is used to develop a convolutional neural network for classifying soil by its salinity level. This code contains the data preparation pipeline, model training, and metric evaluation.

## Dataset creation
<img width="729" height="391" alt="image" src="https://github.com/user-attachments/assets/0b366251-eec0-4ef3-8d34-816b1fc88afa" />
<p>Three different soil types (loam, clay loam, and sandy loam) were provided 3 different salinity levels (0.2dS/m, 4.4dS/m, and 8.5dS/m) and had 10m long coils of optical fiber with diameters of 10cm were embedded within. Two coils were placed within each vessel, one 10cm below the soil surface and the other 15cm below. 100, 300, 500, 750, and 1000Hz tones were generated above the soil using two suspended speakers. A distributed acoustic sensor interrogated the optical fiber and measured the change in acoustic wave propogation characteristics caused by the different salinity levels. </p>
<p> 11 days of measurements were taken to obtain enough data to train the neural network to be moisture invarient. A single sample contains a specific frequnecy measured by one coil within a soil type of a particular salinity level. Additionally, data augmentation was performed on the training dataset to increase model performance. Days 1 - 10 were used for training and validation while day 11 was withheld for testing after the model was created. </p>

## Model results 
After training for 150 epochs on 6300 samples, the model achieved accuracy scores of 96% and 92% on the validation and test datasets, respectively. Suggesting that the model is able to accurately classify soils with varying salinities between 0 and 8.5 dS/m.

## Notes about code
The code provided is designed to load in all required data, prepare the datasets, and develop the model. Due to the DAS's data size, the raw files have not been included in this repository. Please contact steven.binder@uga.edu if you are interested in obtaining the raw data.

## Author 
Steven Binder
