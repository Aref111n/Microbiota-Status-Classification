## Project Overview
Need to develop a model to classify patients' gut microbiota status into three categories ('Optimal', 'Suboptimal', and 'At Risk') using health indicators, medical history, dietary habits, and lifestyle factors.

## Dataset Description
The dataset contains 53 columns and 10,000 rows. The target column is the "Current status of microbiota", where there are three columns:
- Optimal
- Suboptimal
- At Risk
The distribution of these classes is:

| Class | Quantity |
|-------|----------|
| Optimal     | 4554      |
| Suboptimal    | 4672      |
| At Risk     | 774       |

This shows that the dataset is imbalanced. The dataset significantly contains Numerical, Categorical and Multivalued Columns.
## Setup Instructions
Use any environment that supports ipynb files.

## Key Results
| Model                                    | Accuracy | Precision | Recall | F1 (macro) |
|------------------------------------------|----------|-----------|--------|------------|
| Logistic Regression                      | 0.6400   | 0.6400    | 0.6500 | 0.6400     |
| Random Forest                            | 0.6600   | 0.6600    | 0.6600 | 0.6600     |
| XgBoost                                  | 0.6561   | 0.6533    | 0.6560 | 0.6546     |
| ANN                                      | 0.6744   | 0.6759    | 0.6743 | 0.6741     |
| LightGBM                                 | 0.5500   | 0.5700    | 0.6100 | 0.5800     |
| MLP with feature interaction             | 0.6687   | 0.6669    | 0.6686 | 0.6571     |
| Stacking (LR+MLP+XgBoost)                | 0.6695   | 0.6690    | 0.6693 | 0.6691     |
| Hierarchical XgBoost                     | 0.9182   | 0.9181    | 0.9183 | 0.9182     |
| Hierarchical Tab Transformer             | 0.6529   | 0.6559    | 0.6596 | 0.6557     |
| Hierarchical XgBoost with Bayesian Optimization | 0.9281   | 0.9281    | 0.9281 | 0.9280     |
| Hierarchical XgBoost with Optuna         | 0.9258   | 0.9258    | 0.9258 | 0.9258     |

The Hierarchical XgBoost with Bayesian Optimization achieved the highest performance, with an F1-score of 0.9280.
