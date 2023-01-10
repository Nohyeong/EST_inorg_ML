# Exploring the knowledge attained by machine learning on ion transport across polyamide membranes using explainable artificial intelligence

```
Python version: 3.7.13 
SHAP version: 0.41.0
Bayesian optimization: 1.2.0
```

This file is the guidance for running machine learning models for predicting inorganic ion rejections by reverse osmosis and nanofiltration membranes. All the codes were run and tested on Google Colab. Jupyter notebook or other Python integrated development environments (IDE)/code editors can be also used to run the codes.

## Description of codes and dataset
The machine learning model for predicting single salt rejection can be found from 'single_code.ipynb'. You can find the dataset for single salt solutions from 'Single_salt' tab in 'Supplementary_data_final.xlsx'. The code for cation and anion rejection prediction can be seen from 'mix_code.ipynb'. The dataset for cation and anion rejection can be found from the 'Cation' and 'Anion' tabs in 'Supplementary_data_final.xlsx'. The list of input variables and their units are described in 'input_variables' tab in 'Supplementary_data_final.xlsx'.

## Uploading the files on Google Colab
Download the files, and upload the codes (mix_code.ipynb and single_code.ipynb) and dataset (Supplemenatary_data_final.xlsx) on Google Drive or save them on your local computer (for Jupyter notebook). Downloading and uploading files may take about a minute. If you use Google Colab, you need to permit access to Google Drive by running the code

```
from google.colab import drive
drive.mount('/gdrive', force_remount=True)
```

## Installing the required libraries
To run the codes, Bayesian-optimization and SHAP should be installed. You can install those libraries by running 

```
!pip install bayesian-optimization
!pip install shap
```

Other libraries, such as XGBoost and sklearn, are already installed in Google Colab. If not, you may also need to install those libraries.

## Dataset
The dataset for predicting membrane performance for single salt, cation, and anion in mixture salt solutions are separately collected from the literature. In order to train a machine learning model, you need to choose the dataset (i.e., single salt, cation, and anion) and testing data. Training/validation data will be automatically assigned after determining the testing dataset. The data with the same type of single salt/ion from the same reference are assigned as testing data, and the rest of the data are used for training. By setting k values, you can change the testing dataset.

## Making predictions
After determining the testing data by setting k (ID for ref_ion), the machine learning model will use training/validation data to optimize the model and provide the predictions. 

## Calculating SHAP values and obtaining SHAP summary, SHAP importance, and SHAP dependence plots.
After running the code for calculating SHAP values, the SHAP summary plot will appear. You may see the SHAP importance plot without any changes to the codes. For the SHAP dependence plot, the variable should be assigned (e.g., MWCO, charge_product...).


