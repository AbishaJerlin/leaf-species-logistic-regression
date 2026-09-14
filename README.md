# Leaf Species Classification with Logistic Regression

This repository contains my Statistical Data Science coursework on classifying two leaf species using leaf length and leaf width.

I compared a standard logistic regression model with polynomial logistic regression models from degree 2 to degree 5. The aim was to see how increasing model complexity affected classification performance and the shape of the decision boundary.

## What I did

The analysis includes:

- cleaning and preparing the leaf measurement data
- exploring the relationship between leaf length, leaf width and species
- creating a 70/30 train and test split
- fitting a linear logistic regression model
- fitting polynomial logistic regression models from degree 2 to degree 5
- evaluating the models using accuracy, Kappa, sensitivity and specificity
- comparing decision boundaries
- plotting ROC curves
- checking how increasing model complexity affected performance and overfitting

## Main result

The degree 4 polynomial logistic regression model gave the strongest test performance.

| Model | Accuracy |
|---|---:|
| Linear | 86.18% |
| Degree 2 | 89.43% |
| Degree 3 | 90.24% |
| Degree 4 | **91.06%** |
| Degree 5 | 87.80% |

The results showed that adding non-linearity improved classification up to degree 4. The degree 5 model then performed worse on the test data, suggesting that the additional complexity did not improve generalisation.

## Technologies used

- R
- Jupyter Notebook
- Logistic Regression
- Polynomial Logistic Regression
- ggplot2
- caret
- pROC
- patchwork

## Project structure

```text
leaf-species-logistic-regression/
├── data/
│   └── leaf_data.csv
├── notebooks/
│   └── leaf_species_analysis.ipynb
├── images/
│   ├── leaf-length-width-scatter.png
│   ├── linear-decision-boundary.png
│   ├── degree4-decision-boundary.png
│   ├── degree5-decision-boundary.png
│   ├── leaf-density-plots.png
│   ├── model-accuracy-comparison.png
│   ├── model-performance-metrics.png
│   └── roc-curves.png
├── .gitignore
├── LICENSE
└── README.md
```

## Example outputs

### Leaf measurements

<img width="840" height="840" alt="leaf-length-width-scatter" src="https://github.com/user-attachments/assets/cdde39b2-9de9-4e79-9f64-d5b7580df94f" />

### Degree 4 decision boundary

<img width="840" height="840" alt="degree4-decision-boundary" src="https://github.com/user-attachments/assets/5654c69d-b057-4c90-9f65-a2c58e466fe0" />

### Degree 5 decision boundary

<img width="840" height="840" alt="degree5-decision-boundary" src="https://github.com/user-attachments/assets/56f9066d-531a-4420-b0d5-155db309e98b" />

### Accuracy comparison

<img width="840" height="840" alt="model-accuracy-comparison" src="https://github.com/user-attachments/assets/6b54d8ef-a256-4087-afde-87c8f8fad80d" />

### ROC curves

<img width="840" height="840" alt="roc-curves" src="https://github.com/user-attachments/assets/628f415b-079e-49b2-aee6-d7459eef2c34" />

## Running the notebook

The analysis notebook is available at:

`notebooks/leaf_species_analysis.ipynb`

The dataset is stored at:

`data/leaf_data.csv`

When running the notebook from the `notebooks` folder, the dataset can be loaded using:

```r
data_6908119 <- read.csv("../data/leaf_data.csv")
```

The main packages used in the analysis are:

```r
library(ggplot2)
library(caret)
library(pROC)
library(patchwork)
```

Open the notebook in Jupyter Notebook or JupyterLab and run the cells in order to reproduce the analysis and visualisations.

## What I learned

This coursework helped me understand how model complexity affects classification performance.

The linear logistic regression model gave me a useful baseline, but it could not fully capture the curved separation between the two species. Adding polynomial terms improved the model up to degree 4.

The degree 5 model then performed worse on the test data, which showed that making a model more complex does not always improve its ability to generalise.

The decision boundary plots were also useful because they made it easier to visually compare how each model separated the two species. Looking at these plots alongside accuracy, sensitivity, specificity and ROC curves gave a clearer picture of overall model performance.

## Data

The dataset used for this analysis is included in `data/leaf_data.csv`.

It contains leaf length, leaf width and species information used to train and evaluate the classification models.

## License

This project is licensed under the MIT License.
