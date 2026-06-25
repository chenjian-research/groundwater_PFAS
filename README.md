Dada and code for the Manuscript entitled "Achieving a 25% reduction in PFAS exceedance areas in European groundwater through key point source mitigation"
Overview

In this manuscript, we developed an extreme gradient boosting (XGBoost) model to predict the probability of PFAS concentrations in groundwater exceeding the 100 ng/L EU Drinking Water Guideline. The machine-learning models were implemented in Jupyter Notebook (V.7.0.8) using Python 3.12.

Hardware requirements:

Only a standard modern computer is needed, with sufficient RAM to support in-memory processing of datasets.

Software requirements：

These analyses are compatible with Windows, macOS, and Linux operating systems.

Installation Guide：

Python is developed under an OSI-approved open-source license, making it freely usable and distributable. Python can be easy to pick up following the installation guide on the official website:

Installing Python: https://www.python.org/downloads/

Installing Jupyter: https://jupyter.org/install

Installing Python typically takes several minutes up to twenty minutes, depending on your internet connection and system setup.

Package dependencies:

After installing Python and Jupyter Notebook, you need install the following Python packages (if not already installed): pip install scikit-learn, xgboost, shap, matplotlib, pandas, numpy, statsmodels, imblearn, geopandas Installation may take approximately 10-20 minutes, depending on your internet speed and system specifications.

Running the demo:

We have provided a demonstration notebook (‘Demo for E. coli.ipynb’) and dataset files (‘Demo_ecoli.csv’  for training/testing and ‘Demo_prediction.csv’ (Demo_prediction.7z) for prediction). These allow you to reproduce our results for predicting PFAS exceedance in European groundwater at a 1 km resolution using the XGBoost model.

Step-by-Step Instructions:

Model training and evaluation (take ‘Demo for E. coli.ipynb’ as an example)

In the first cell, you can load and run the code to input the training and test sets (‘Demo_ecoli.csv’). The code will train the XGBoost model and evaluate its performance using metrics such as accuracy, specificity, sensitivity, and AUC (area under the ROC curve).

Plot ROC curve

In the second cell, you can run the provided code to visualize the ROC curve and output the AUC value of the XGBoost model.

SHAP analysis

The third cell runs SHAP (SHapley Additive exPlanations) analysis to further interpret the model.

Feature importance

In the fourth cell, you can run the code to determine the relative contributions of each input feature.

Threshold identification

In the fifth cell, you can execute the code to identify the threshold point where sensitivity equals specificity.

Prediction on riverine grid cells

In the sixth cell, you can input the prediction dataset (Demo_prediction.csv) and run the code to predict pharmaceutical exceedance for E. coli in 223,152 global riverine grid cells.

Global visualization

In the seventh cell, you can run the code to map the pharmaceutical exceedance for E. coli in global rivers at 2 km resolution.

The outputs from this demo will match the results presented in our manuscript.

Support and Feedback

We welcome any questions, comments, or suggestions regarding the code, data, or analysis workflow.

Thank you for your interest in our work!

Best wishes,

Jian (chenjianhk@ust.hk)
