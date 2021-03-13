# Predicting Thermodynamic Stability of Perovskite Oxides
Weixi Yao, Seung-Jae Bang, William Yu, Jiaying Chen, Yiming Huang, Caroline Rutherford

Supervised by Prof. Simon Billinge

Watch Youtube video here: https://www.youtube.com/watch?v=xiM2rrrJC8k&t=1s

## Project Description and Motivation
This project is offered as an improvement over the original Li, Jacobs et. al paper 'Predicting the thermodynamic stability of perovskite oxides using machine learning models.'
in which machine learning methods are used to approximate traditional Density Functional Theory (DFT) methods of calculating phase stability of perovskite compounds.

## Methodology
Split into classification and regression tasks using Energy Above Convex Hull (Ehull). Encode > 40 meV/atom as unstable compounds, encode < 40 meV/atom as stable compounds, becoming a binary classification task.
Regression predicts range of Ehull values.

To improve on the original paper, the team devised multiple methods:
- Subset compounds by A-site elements and B-site elements and develop model to predict for each subgroup
- Implement algorithmic oversampling (see smote_smogn.ipynb), which oversamples data for each cross-validation fold
- Enhance EDA demonstrated in paper, by using variance thresholds and removing highly correlated features, as well as optimize RFE

## Results
The classification task demonstrated by the team was shown to improve upon the original paper with an f1 score of 0.919 ± 0.020, wheras the paper was 0.88 ± 0.03.
The regression task did not improve.
