# Predicting Patient Readmissions.
## Machine Learning Model Evaluation: Logistic Regression, Random Forest and XGBoost
## Project Overview
This project demonstrates the evaluation of three popular machine learning models—**Logistic Regression**, **Random Forest**, and **XGBoost**—on a multiclass classification task. The goal of this project is to predict a target variable with multiple classes using various machine learning algorithms. The models were optimized using **Grid Search** to fine-tune hyperparameters for better performance. Evaluation metrics like **Confusion Matrix**, **Classification Report**, and **ROC-AUC** were used to assess the models' performance.
## Table of Contents
- [Installation](#installation)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Model Evaluation](#model-evaluation)
- [Challenges and Future Improvements](#challenges-and-future-improvements)
## Installation

To run this project, you need to have Python installed along with the following dependencies:

1. **scikit-learn**: A machine learning library for Python.
2. **xgboost**: A library for gradient boosting algorithms.
3. **matplotlib**: A library for plotting and visualization.
4. **numpy**: A library for numerical computations.
5. **pandas**: A library for data manipulation and analysis.

You can install the required libraries using `pip`:

```bash
pip install scikit-learn xgboost matplotlib numpy pandas
```

## Project Structure

The project contains the following key files:

- `main.py`: The main Python script where the models are trained, evaluated, and hyperparameters are optimized.
- `data/`: A directory containing the dataset used for training and testing the models.
- `requirements.txt`: A file listing all the necessary Python packages for the project.
- `README.md`: This file, which provides an overview of the project, installation instructions, and usage.

## How to Run

1. **Clone the repository**:
   - First, clone the repository to your local machine:
   
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Prepare the dataset**:
   - Ensure that the dataset is available in the `data/` directory. The dataset should be a CSV file containing the features and target variable.

3. **Run the script**:
   - Once the environment is set up and the dataset is ready, you can run the `main.py` script to train and evaluate the models:
   
   ```bash
   python main.py
   ```

4. **Model Evaluation**:
   - The script will output the evaluation results for each model, including the **Confusion Matrix**, **Classification Report**, and **ROC-AUC** score (if applicable). It will also print warnings if any issues arise during the evaluation.

## Model Evaluation

The models are evaluated using the following metrics:

1. **Confusion Matrix**: Displays the true positive, false positive, true negative, and false negative values for each class.
2. **Classification Report**: Provides the precision, recall, f1-score, and support for each class.
3. **ROC-AUC Score**: Measures the performance of the model by calculating the area under the Receiver Operating Characteristic (ROC) curve. The score is calculated only for binary classification tasks or multiclass classification when the class probabilities are aligned correctly.

### Best Hyperparameters for XGBoost:
- **Learning Rate**: 0.01
- **Max Depth**: 3
- **Number of Estimators**: 100

## Challenges and Future Improvements

- **Class Imbalance**: The models performed poorly for class 0, which might indicate an imbalance in the dataset. Future work could explore techniques such as oversampling, undersampling, or class weighting to address this issue.
- **Hyperparameter Tuning**: Although Grid Search was used to optimize hyperparameters, further fine-tuning of model parameters could improve performance.
- **ROC-AUC Calculation**: Issues with mismatched class probabilities led to warnings and skipped ROC-AUC calculations. Ensuring proper alignment of predicted probabilities with the test set labels is necessary for accurate evaluation.
