## Setup & Installation

### Clone the Repository

To begin, clone the repository to your local machine:

```bash
git clone https://github.com/yourusername/wine-quality-prediction.git
cd wine-quality-prediction
```

### Create and Activate a Virtual Environment

Create a virtual environment to manage dependencies:

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows, use .venv\Scripts\activate
```

### Install Dependencies

Install the required Python libraries by running:

```bash
pip install -r requirements.txt
```

If you don’t have the `requirements.txt` file yet, generate it by running:

```bash
pip freeze > requirements.txt
```

### Data File

Download the dataset (`winequality-red.csv`) from [UCI Wine Quality Data](https://archive.ics.uci.edu/ml/datasets/wine+quality), and save it in the root directory of the project.

## Data Description

The dataset consists of 1599 samples with 12 features, as outlined below:

### Features:

- **Fixed acidity**: Mostly tartaric acid.
- **Volatile acidity**: Primarily acetic acid (vinegar).
- **Citric acid**: Adds freshness and flavor.
- **Residual sugar**: Sugar remaining after fermentation.
- **Chlorides**: Salt content.
- **Free sulfur dioxide**: Protects wine from microbes.
- **Total sulfur dioxide**: Sum of free and bound forms.
- **Density**: Related to sugar content.
- **pH**: Acidity level (lower values indicate more acidity).
- **Sulphates**: Antioxidant and microbial stabilizer.
- **Alcohol**: Percentage of alcohol by volume.

### Target Variable:

- **Quality**: An integer score from 0 to 10 given by tasters. This is converted into three categories for classification:

  - **Low**: Quality 3-4
  - **Medium**: Quality 5-6
  - **High**: Quality 7-8

## Modeling & Evaluation

### Data Preprocessing

1. **Data Cleaning**: Handle missing values, outliers, and other inconsistencies in the dataset.
2. **Feature Engineering**: Transform the `quality` target variable into three categories (low, medium, high) and assign numeric values (0, 1, 2) for classification.

### Models Evaluated

The following machine learning models were evaluated to predict the wine quality:

1. **Random Forest**: 200 decision trees with a maximum depth of 10.
2. **MLP Classifier**: A simple Multilayer Perceptron (neural network) with one hidden layer.

### Evaluation Metrics

Models were evaluated based on:

- **Accuracy**: The proportion of correct predictions made by the model.
- **F1-Score**: A weighted average of precision and recall, useful for imbalanced datasets.

### Performance Summary

The **Random Forest** model performed significantly better than the **MLP Classifier**:

- **Random Forest**: 
  - Test Accuracy: **88.12%**
  - F1 Score: **85.96%**

- **MLP Classifier**:
  - Test Accuracy: **84.38%**
  - F1 Score: **80.73%**

The Random Forest model achieved higher test accuracy and F1 score, demonstrating its better ability to generalize on unseen data.


