
# Crop Recommendation System

This repository contains a **Crop Recommendation System** project developed using machine learning models to recommend suitable crops based on various environmental and soil factors. The system uses different classification models to predict which crop would perform best in specific conditions.

## Features

- Predicts crop recommendations based on input features such as temperature, humidity, rainfall, and soil parameters.
- Implements various machine learning models and evaluates their performance based on accuracy.
- Helps farmers and agricultural experts make data-driven decisions.

## Models Used

Several machine learning models were evaluated for crop recommendation prediction. Below are the models used and their respective accuracies:

- **Logistic Regression**: 96.36%
- **Gaussian Naive Bayes (GaussianNB)**: 99.55%
- **Support Vector Classifier (SVC)**: 96.82%
- **K-Nearest Neighbors (KNeighborsClassifier)**: 95.91%
- **Decision Tree Classifier**: 98.86%
- **Extra Trees Classifier (ExtraTreeClassifier)**: 92.95%
- **Random Forest Classifier (RandomForestClassifier)**: 99.32%
- **Bagging Classifier (BaggingClassifier)**: 98.64%
- **Gradient Boosting Classifier (GradientBoostingClassifier)**: 98.18%
- **AdaBoost Classifier**: 14.09% (performs poorly, further analysis needed)

The best-performing models were **Gaussian Naive Bayes** and **Random Forest**, both achieving accuracies above 99%. **AdaBoost Classifier** performed significantly worse, which could be due to issues with data quality, model configuration, or hyperparameters.

## Dataset

The dataset used for training and prediction contains the following columns:

- **N**: Nitrogen content in the soil
- **P**: Phosphorus content in the soil
- **K**: Potassium content in the soil
- **Temperature**: Temperature in °C
- **Humidity**: Humidity percentage
- **pH**: Soil pH level
- **Rainfall**: Rainfall in mm

Example data from the dataset:

| N  | P  | K  | Temperature (°C) | Humidity (%) | pH   | Rainfall (mm) |
|----|----|----|------------------|--------------|------|---------------|
| 90 | 42 | 43 | 20.88            | 82.00        | 6.50 | 202.94        |
| 85 | 58 | 41 | 21.77            | 80.32        | 7.04 | 226.66        |
| 60 | 55 | 44 | 23.00            | 82.32        | 7.84 | 263.96        |
| 74 | 35 | 40 | 26.49            | 80.16        | 6.98 | 242.86        |
| 78 | 42 | 42 | 20.13            | 81.60        | 7.63 | 262.72        |

## Setup and Usage

### Clone the Repository

Clone the repository to your local machine using the following command:

```bash
git clone https://github.com/Deep130804/Crop-Recommendation-System.git
cd Crop-Recommendation-System
```

### Install Dependencies

Make sure to install the necessary dependencies. If a `requirements.txt` file is available, you can install all the required libraries:

```bash
pip install -r requirements.txt
```

Alternatively, install dependencies like `scikit-learn`, `pandas`, `numpy`, and `Flask` manually.

### Run the Application

After cloning the repository, run the application using the following command:

```bash
python app.py
```

This will start the Flask server. You will then see an interface where you can enter values for N, P, K, Temperature, Humidity, pH, and Rainfall. After entering these values, the system will recommend the most suitable crop based on the entered conditions.
