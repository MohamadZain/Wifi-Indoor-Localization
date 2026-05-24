# WiFi Indoor Localization

Machine learning–based indoor localization system using WiFi fingerprinting and the UJIIndoorLoc dataset.

## Overview

The goal of the project is to predict indoor building location, floor level, and physical coordinates using WiFi RSSI fingerprint data collected from multiple wireless access points.

The project also compares multiple machine learning models for both classification and regression tasks in indoor positioning environments where GPS signals are unreliable.

## Features

* WiFi fingerprint–based indoor localization
* Building and floor classification
* Coordinate regression prediction
* RSSI preprocessing and scaling
* Model comparison and evaluation
* Multi-output classification and regression

## Models Used

### Classification Models

* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest

### Regression Models

* Linear Regression
* MLP Regressor
* Gradient Boosting Regressor

## Exploratory Data Analysis

### RSSI Signal Strength Distribution

The histogram below shows the distribution of WiFi RSSI signal strengths across access points in the dataset. Most values fall between -100 dBm and -60 dBm, indicating generally weak indoor WiFi signal conditions caused by walls, interference, and distance from access points.

<img width="533" height="396" alt="rssi_signal distribution" src="https://github.com/user-attachments/assets/6ef9a560-3592-478d-b7b0-af733d4a0455" />

## Results

### Classification Results

| Model         | Building Accuracy | Floor Accuracy | Precision | F1 Score |
| ------------- | ----------------- | -------------- | --------- | -------- |
| KNN           | 98.2%             | 84.1%          | 0.831     | 0.836    |
| Decision Tree | 97.6%             | 80.3%          | 0.798     | 0.800    |
| Random Forest | 99.5%             | 89.3%          | 0.889     | 0.891    |

### Regression Results

| Model             | RMSE (m) | MAE (m) | R²   |
| ----------------- | -------- | ------- | ---- |
| Linear Regression | 23.4     | 17.8    | 0.61 |
| MLP Regressor     | 10.2     | 7.6     | 0.87 |
| Gradient Boosting | 8.7      | 6.3     | 0.91 |

## Best Performing Models

Random Forest achieved the best classification performance with 99.5% building accuracy and 89.3% floor accuracy, outperforming KNN and Decision Tree models.

For coordinate prediction, Gradient Boosting achieved the lowest positioning error with an RMSE of 8.7 meters, making it the strongest regression model in this project.

The results show that advanced models such as Random Forest and Gradient Boosting performed better than simpler baseline models on noisy WiFi signal data.

## Dataset

UJIIndoorLoc Dataset:
https://archive.ics.uci.edu/dataset/310/ujiindoorloc

The full dataset was not uploaded due to size limitations.

## Tech Stack

* Python
* Scikit-learn
* Pandas
* NumPy
* Matplotlib

