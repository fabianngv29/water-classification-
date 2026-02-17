# IoT-Based Residential Water Consumption Dataset

This repository contains a labeled dataset used for the classification of residential water consumption events based on hydrostatic pressure sensor measurements in a domestic water storage tank.

## Dataset Description

Each row in the dataset represents a detected water consumption event. The features were extracted from water level measurements acquired through an IoT-based monitoring system.

### Columns

- **group_id**: Unique identifier of the consumption event.
- **Initial_Liters**: Estimated water volume (in liters) at the beginning of the event.
- **Final_Liters**: Estimated water volume (in liters) at the end of the event.
- **Initial_mA**: Initial sensor output in milliamperes (hydrostatic pressure signal).
- **Final_mA**: Final sensor output in milliamperes.
- **Consumed_Liters**: Estimated volume of water consumed during the event.
- **label**: Activity class associated with the event.

### Activity Labels

The dataset includes five residential water usage categories:

- Stable State  
- Tank Refilling  
- Toilet Flushing  
- Washing Clothes  
- Taking a Bath  

## Feature Rationale

The classification task was performed using numerical features derived from water level measurements. The selected variables (Initial_Liters, Final_Liters, Initial_mA, Final_mA, and Consumed_Liters) capture:

- The initial state of the storage system  
- The final state after the event  
- The magnitude of the water consumption  

This feature combination provides sufficient descriptive information to distinguish between different residential water usage activities.

## Dataset Size

The dataset consists of **4,396 labeled water consumption events**, covering all defined activity classes and ensuring statistical representativeness for machine learning model training and evaluation.

## Purpose

This dataset was used to train and evaluate supervised machine learning models (e.g., SVM, Random Forest, KNN, Decision Tree, and RNN/LSTM) for automated classification of residential water consumption patterns.

