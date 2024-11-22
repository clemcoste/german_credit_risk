# German Credit Risk Analysis

This repository contains an analysis of the **German Credit Risk dataset**. The objective of this project is to evaluate credit risk and predict whether a customer falls into the "good" or "bad" risk category using machine learning models.

## 📂 Project Structure

The repository is organized as follows:
    
    .
    ├── data
    │   ├── raw                # Raw data files (original dataset)
    │   ├── processed          # Processed data files (encoded)
    ├── notebooks
    │   ├── german_credit_risk_analysis.ipynb  # Jupyter notebook with the analysis
    ├── reports
    │   ├── figures            # Visualizations generated during analysis
    ├── requirements.txt       # Python dependencies for the project
    ├── README.md              # Project overview (this file)

## 📊 Dataset Overview

The **German Credit Risk** dataset includes information on 1,000 customers with the goal of predicting their credit risk. Key features of the dataset include:

- **Target Variable**: `Risk` - indicates whether the customer is a good or bad credit risk.
- **Input Variables**:
          The selected attributes are:
        <ol>
        <li>Age (numeric)</li>
        <li>Sex (text: male, female)</li>
        <li>Job (numeric: 0 - unskilled and non-resident, 1 - unskilled and resident, 2 - skilled, 3 - highly skilled)</li>
        <li>Housing (text: own, rent, or free)</li>
        <li>Saving accounts (text - little, moderate, quite rich, rich)</li>
        <li>Checking account (numeric, in DM - Deutsch Mark)</li>
        <li>Credit amount (numeric, in DM)</li>
        <li>Duration (numeric, in month)</li>
        <li>Purpose (text: car, furniture/equipment, radio/TV, domestic appliances, repairs, education, business, vacation/others)</li>
        </ol>

## 🔍 Analysis Steps

1. **Data Preprocessing**:
   - Handling missing values in features like `Saving accounts` and `Checking account`.

2. **Exploratory Data Analysis (EDA)**:
   - Univariate analysis : plot, treemaps, and creation of categories for Purpose
   - Bivariate analysis
   - Overview : Pairplot

3. **Encoding categorical variables for compatibility with machine learning algorithms**:
   - Encoding categorical data
   - Correlation heatmap

5. **Model Training and Evaluation**:
   - Splitting the dataset
   - Standardization
   - Models building:
     - Naive Bayes
     - k-Nearest Neighbors (KNN)
     - XGBoost (XGB)
   - Metrics for evaluation:
     - Accuracy
     - F1-score
     - ROC-AUC

4. **Model synthesis and conclusion**:
   - ROC Curve
   - The XGBoost model achieved the best performance across all metrics, making it the recommended choice for deployment.

## 🧰 Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/clemcoste/german_credit_risk.git
   cd german_credit_risk

2.	Create venv and install the required dependencies:
    ```bash
    python -m venv venv
    pip install -r requirements.txt

3.	Open the notebook on Visual Studio Code and select venv

## 📈 Figures

All visualizations and figures generated during the analysis are stored in the reports/figures directory. These include:
   - Feature distributions
   - Correlation heatmaps
   - Model performance comparisons

## 🛠️ Requirements

For the full list of dependencies, see the requirements.txt file.

Contributions are welcome! Feel free to submit issues or pull requests if you have suggestions for improvement.

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for more details.
