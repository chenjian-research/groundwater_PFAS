Dada and code for the manuscript entitled "Achieving a 25% reduction in PFAS exceedance areas in European groundwater through key point source mitigation" by Jian Chen, Xiangru Zhang*, Nigel Graham, Lee Blaney and Gang Yu.

Overview

In this manuscript, we developed an extreme gradient boosting (XGBoost) model to predict the probability of PFAS concentrations in groundwater exceeding the 100 ng/L EU Drinking Water Guideline. The machine-learning model was implemented in Jupyter Notebook (V.7.0.8) using Python 3.12.

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

We have provided a demonstration notebook (‘Europe_groundwater_PFAS_DEMO.ipynb’) and dataset files (‘traindata1.csv’) for training/testing and ‘ML_output.db’ (you can download from: https://pan.baidu.com/disk/main?from=homeFlow#/index?category=all&path=%2FPFAS_groundwater) for prediction. These allow you to reproduce our results for predicting PFAS exceedance in European groundwater at a 1 km resolution using the XGBoost model.

Step-by-Step Instructions:
 
Dataset division

In the first cell, you can load and run the code to input the training and test sets. All grid cells were grouped into 24 spatial blocks using the K-Means clustering algorithm based on their geographic coordinates. These blocks were randomly assigned to training (70%) and test (30%) sets. 

Model training and evaluation

In the second cell, the code will train the XGBoost model and evaluate its performance using metrics such as accuracy, specificity, sensitivity, and AUC (area under the ROC curve).


Plot ROC curve

In the third cell, you can run the code to visualize the ROC curve and output the AUC value of the XGBoost model.

Determine the cutoff

In the fourth cell, you can execute the code to identify the threshold point where sensitivity equals specificity.

SHAP analysis

The fifth cell runs SHAP (SHapley Additive exPlanations) analysis to further interpret the model.

Feature importance

In the sixth cell, you can run the code to determine the relative contributions of each input feature.

Prediction on riverine grid cells

In the seventh cell, you can input the prediction dataset (ML_output.db) and run the code to predict PFAS exceedance in 10,921,280 groundwater grid cells.

Map visualization

In the eighth cell, you can run the code to map the PFAS exceedance in European groundwater at 1 km resolution (europecountry3.shp and europe_1km_grid.shp can download from: https://pan.baidu.com/disk/main?from=homeFlow#/index?category=all&path=%2FPFAS_groundwater).


The outputs (Europe_groundwater_PFAS_DEMO.html) from this demo will match the results presented in our manuscript.

Support and Feedback

We welcome any questions, comments, or suggestions regarding the code, data, or analysis workflow.

Thank you for your interest in our work!

Best wishes,

Jian Chen (PhD) 

The Hong Kong University of Science and Technology

Email: chenjianhk@ust.hk
