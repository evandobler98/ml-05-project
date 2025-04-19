# Red Wine Quality Prediction

This project aims to predict the quality of red wine based on various physicochemical features. We utilize machine learning classification models to build a predictive system. The dataset used for this project contains attributes related to wine quality, including features like acidity, sugar content, pH, alcohol percentage, and more. The primary goal is to classify the wine quality into three categories: low, medium, and high.

## Table of Contents

- [Project Overview](#project-overview)
- [Setup & Installation](#setup--installation)
- [Data Description](#data-description)
- [Modeling & Evaluation](#modeling--evaluation)
- [Conclusions](#conclusions)
- [License](#license)

## Project Overview

In this project, we build a classification model to predict the quality of red wine based on its physicochemical attributes. The main steps include:

1. **Data Exploration**: Analyzing and understanding the dataset.
2. **Data Preparation**: Cleaning the data, encoding the target variable, and splitting the dataset into training and testing sets.
3. **Model Selection**: Evaluating several classification models, including Random Forest and MLP Classifier, to identify the best model for predicting wine quality.
4. **Performance Evaluation**: Using performance metrics such as accuracy and F1-score to evaluate and compare the models.

## Setup & Installation

Follow the steps below to set up the environment and run the project.

### Prerequisites

Ensure you have Python 3.x installed on your machine. This project also requires some Python libraries which you can install using `pip`.

### Clone the Repository

```bash
git clone https://github.com/yourusername/wine-quality-prediction.git
cd wine-quality-prediction```

Create and Activate Virtual Environment
bash
Copy code
python -m venv .venv
source .venv/bin/activate  # On Windows, use .venv\Scripts\activate
Install Dependencies
bash
Copy code
pip install -r requirements.txt
You can create the requirements.txt file using:

bash
Copy code
pip freeze > requirements.txt
Data File
Download the dataset (winequality-red.csv) from UCI Wine Quality Data and save it in the root directory of the project.

Data Description
The dataset contains 1599 samples and 12 columns:

Features:
fixed acidity: Mostly tartaric acid.

volatile acidity: Mostly acetic acid (vinegar).

citric acid: Can add freshness and flavor.

residual sugar: Remaining sugar after fermentation.

chlorides: Salt content.

free sulfur dioxide: Protects wine from microbes.

total sulfur dioxide: Sum of free and bound forms.

density: Related to sugar content.

pH: Acidity level (lower = more acidic).

sulphates: Antioxidant and microbial stabilizer.

alcohol: % alcohol by volume.

Target Variable:
quality: Integer score (0 to 10) rated by wine tasters. For modeling purposes, we categorize this into three labels:

Low: Quality 3-4

Medium: Quality 5-6

High: Quality 7-8

Modeling & Evaluation
Data Preprocessing
Data Cleaning: Missing values and outliers are handled (if applicable).

Feature Engineering: We convert the quality target variable into labels (low, medium, high) and numeric labels (0, 1, 2) for classification.

Models Evaluated:
We evaluate the following machine learning models for wine quality prediction:

Random Forest (200 trees, max_depth=10)

MLP Classifier (Multilayer Perceptron neural network)

Evaluation Metrics:
Models are evaluated using the following metrics:

Accuracy: Measures the overall accuracy of the model.

F1-Score: Weighted average of precision and recall, providing a balance between the two.

Performance Summary
The Random Forest model achieved a test accuracy of 88.12% and an F1 score of 85.96%. On the other hand, the MLP Classifier showed a test accuracy of 84.38% and an F1 score of 80.73%.


