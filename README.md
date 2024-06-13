# Multi-Threshold Analysis
This repo contains a workflow for classification of chemical compounds as active or inactive based on experimental outputs and a set of previously computed descriptors. Classification is performed via sci-kit learn's
DecisionTreeClassifier and yields models that can be both interpretable and predictive.

# Installation
A conda environment is provided in the multithreshold_env.yml or multithreshold_env.txt files. To create the environment, run\
`conda env create --file=multithreshold_env_win.yml`\
or\
`conda env create --file=multithreshold_env_lin.yml`\
depending on your opperating system and set the multithreshold environment as the kernel for the Jupyter notebook.

# Requirements
If you'd prefer to create your own environment, here is a list of known dependencies:
1. Python 3.9.16
2. Numpy 1.23.5
3. Pandas 1.5.3
4. Matplotlib 3.7.0
5. Ipykernel 6.15.0
6. Scikit-learn 1.2.1
7. Openpyxl 3.0.10
8. Ipympl 0.9.3

An environment with these packages can be created using the command\
`conda create -n mta_test -c conda-forge python=3.9.16 numpy=1.23.5 pandas=1.5.3 matplotlib=3.7.0 ipykernel=6.15.0 scikit-learn=1.2.1 openpyxl=3.0.10 ipympl=0.9.3`

# Usage
The full workflow can be run via the Multi-Threshold Analysis.ipynb notebook. Supporting functions and classes can be found in the hotspot_utils.py and hotspot_classes.py files respectively. Input data should be formatted
as shown in the 'InputData/Multi-Threshold Analysis Data.xlsx' file 'Suzuki Yields and Parameters sheet, with a column of compound identifiers, all output columns, then all feature columns. The first row should contain x#
labels for each feature and the second row should be column names.
