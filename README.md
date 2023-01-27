# Exploring the knowledge attained by machine learning on ion transport across polyamide membranes using explainable artificial intelligence

```
Python version: 3.7.13 
SHAP version: 0.41.0
Bayesian optimization: 1.2.0
```

This file is the guidance for running machine learning models for predicting inorganic ion rejections by reverse osmosis and nanofiltration membranes. All the codes were run and tested on Google Colab. Jupyter notebook or other Python integrated development environments (IDE)/code editors can be also used to run the codes.

## Description on dataset
You can find the dataset for single salt from 'Single_salt' tabs in 'Supplementary_data_final.xlsx'. The dataset for cation and anion rejection can be found from the 'Cation' and 'Anion' tabs in 'Supplementary_data_final.xlsx'. The list of input variables and their units are described in 'input_variables' tab in 'Supplementary_data_final.xlsx'.

## Uploading the files on Google Colab
Upload the machine learning models and dataset (Supplemenatary_data_final.xlsx) on Google Drive or save them on your local computer (for Jupyter notebook). Uploading files may take about a minute. If you use Google Colab, you need to permit access to Google Drive by running the code

```
from google.colab import drive
drive.mount('/gdrive', force_remount=True)
```

## Installing the required libraries
To run the codes, SHAP should be installed. You can install those libraries by running 

```
!pip install shap
```

Other libraries, such as XGBoost and sklearn, are already installed in Google Colab. If not, you may also need to install those libraries.

## Calculating SHAP values and obtaining SHAP summary, SHAP importance, and SHAP dependence plots.
After loading the dataset file and machine learning models, the SHAP summary plot will appear. For the SHAP dependence plot, the variable should be assigned (e.g., MWCO, charge_product...).


<img src="https://t.bkit.co/w_63d449ee8bbeb.gif" />
