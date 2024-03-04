# IDML-1 Machine learning for income classification

## Description
 The primary objective of this project was to construct a binary classification model capable of predicting whether an individual's income exceeds or falls below $50,000 USD. The dataset provided for this task encompassed 15 columns, with the "income" column serving as the dependent variable. Several preprocessing steps were employed to prepare the dataset for modeling.

## Approach
 The notebook starts with Exploratory Data Analysis (EDA) and data preprocessing, then proceeds towards predictive modeling, and lastly, hyperparameter tuning for the best-performing model.

### Dataset and Quality:
 The given dataset consists of 30k rows and 15 columns, with a few categorical columns containing missing values. These missing values were imputed using the mode value for those columns. However, for the income column, there were 25k missing values, along with a significant class imbalance. Mode imputation wasn't a suitable approach for this situation. To impute the income column, two techniques were used:

 1. Distribution-preserving random sampling.
 2. Predictive imputation through logistic regression.

### Modeling:
 Initially, a random baseline model was constructed to assess the performance of other models. Later, logistic regression, decision tree, random forest, and naive Bayes models were constructed on the dataset obtained through predictive imputation. Following this, feature selection was employed using random forest feature selection, and the same models were constructed on this smaller subset of features and evaluated using 10-fold cross-validation. Afterward, the best-performing model, i.e., random forest, was subjected to hyperparameter tuning, and the best parameters were used for re-modeling. The results showed a slight improvement in various performance metrics.





## Directories

The project is structured as follows:

- **bin**: This directory contains the source code files required to run the analysis.
  - `income_classification.ipynb`: This Python script is the main entry point for executing the project. It contains the code that reads the dataset and performs various data processing, modelling and visualization tasks.
 

- **data**: This directory contains the dataset used for the analysis.
  - `einkommen_train`: The CSV file that contains the data used for this project.

- **plots **: This directory contains the plots produced during this project.
## User Guide
To use this project, follow the steps below:

1. Clone the repository: git clone https://github.com/fahaddeshmukh/Income_classification


2. Install the required dependencies: pip install -r requirements.txt



3. Prepare the dataset:
- Place the dataset file (e.g., `einkommen_train`) in the project directory.

4. Run the income_classification.ipynb:



## Contact Information
For any questions, suggestions, or issues, please feel free to contact:

- Name: Fahad Deshmukh

- Email: deshmukh@uni-potsdam.de
