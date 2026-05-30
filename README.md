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

| Model | Building Accuracy | Floor Accuracy | Combined Accuracy | Precision | F1 Score |
|---------|---------|---------|---------|---------|---------|
| KNN | 99.10% | 80.38% | 80.11% | 81.84% | 80.62% |
| Decision Tree | 92.62% | 59.59% | 57.61% | 67.10% | 60.33% |
| Random Forest | 100.00% | 90.64% | 90.64% | 91.21% | 90.63% |

### Regression Results

| Model | RMSE (m) | MAE (m) | R² |
|---------|---------|---------|---------|
| Linear Regression | 47.38 | 32.70 | 0.772 |
| MLP Regressor | 17.12 | 9.86 | 0.967 |
| Gradient Boosting | 22.06 | 14.13 | 0.947 |

## Best Performing Models

Random Forest achieved the strongest classification performance, reaching 100% building accuracy, 90.64% floor accuracy, and 90.64% combined accuracy. It also achieved a floor-level precision of 91.21% and an F1 score of 90.63%, outperforming both KNN and Decision Tree models.

For coordinate prediction, the MLP Regressor achieved the best overall performance with the lowest prediction error (RMSE = 17.12 m, MAE = 9.86 m) and the highest R² score of 0.967, indicating strong predictive accuracy for indoor coordinate estimation.

The results show that advanced machine learning models such as Random Forest and MLP Regressor performed significantly better than baseline approaches for indoor localization using WiFi fingerprint data.

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

