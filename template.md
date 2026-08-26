# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Seeds Dataset Machine Learning Analysis

## Members:
- Vinicius Salvador

## Professors:
### Tutor
- Sabrina Otoni
### Coordinator
- André Godoi Chiovato


## Description

This project applies machine learning techniques to the Seeds Dataset, a collection of geometric measurements taken from kernels belonging to three different varieties of wheat: Kama, Rosa and Canadian. Each sample is described by seven features, including area, perimeter, compactness, kernel length, kernel width, asymmetry coefficient and kernel groove length.

The analysis starts with an exploratory phase, covering descriptive statistics, distribution visualization through histograms and boxplots, outlier detection and a correlation analysis between features. This step reveals strong collinearity among variables such as area, perimeter, width and length, which is an important consideration for models like linear regression or SVM that can be sensitive to multicollinearity.

After the exploratory phase, the dataset goes through a preprocessing pipeline that checks for missing values and applies feature scaling using StandardScaler, preparing the data for algorithms that are sensitive to feature magnitude. The dataset is then split into training and test sets using a 70/30 ratio.

Three classification models are implemented and compared: K-Nearest Neighbors, Support Vector Machine and Random Forest. Each model is first trained with its default configuration and evaluated using accuracy, average precision, average recall and average F1-score. GridSearchCV is then used to search for the best hyperparameters for each model, and the optimized versions are retrained and evaluated using the same metrics, allowing a direct before and after comparison of model performance.


## Folder structure

Among the files and folders present in the root of the project, the following are defined:

- <b>assets</b>: contains the files related to unstructured elements of this repository, such as images.

- <b>data</b>: contains the Seeds Dataset used for the analysis.

- <b>notebooks</b>: contains the Jupyter notebook with the full analysis and model implementation.

- <b>pyproject.toml / poetry.lock</b>: project dependency configuration managed with Poetry.

- <b>README.md</b>: file that serves as a guide and general explanation about the project.

## How to run the code

Prerequisites:
- Python 3.11.9
- Poetry
- Jupyter Notebook or JupyterLab

Steps:
1. Clone the repository.
2. Install the project dependencies with Poetry:
   ```
   poetry install
   ```
3. Activate the environment and open the notebook `notebooks/scikit-learn-ml-analysis.ipynb`.
4. Run the notebook cells in order to reproduce the exploratory analysis, preprocessing, model training and evaluation.


## Release history

* 0.1.0 - 27/11/2025
    * Initial project setup, exploratory data analysis, preprocessing and implementation of KNN, SVM and Random Forest models with GridSearchCV hyperparameter optimization.

## License

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">FIAP GIT MODEL</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> is licensed under <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>
