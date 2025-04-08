# Data-Analysis-for-Business – Multinomial Logistic Regression on Hitters Dataset

In this project, we use the **Hitters** dataset to analyze and model Major League Baseball player salaries using **Multinomial Logistic Regression**, with a strong focus on **data preprocessing**, **model evaluation through cross-validation**, and **model selection**.

---

## Project Files

- `ProjectWork_xx.Rmd`: R Markdown source file with full analysis.
- `ProjectWork_xx.html`: Compiled HTML output.
- `Hitters.csv`: Dataset used for the project.
- `style1.css`: Css added fot the design.

---
## Project Structure

- `01_data_preparation/` – Cleaning and formatting the dataset
- `02_eda/` – Exploratory Data Analysis and visualizations
- `03_clustering_pca/` – Player archetypes via clustering and PCA
- `04_modeling/` – Training, tuning, and evaluating classification models
- `05_report/` – Final results, visual summaries, and conclusions


## Dataset Description

We work with the `Hitters.csv` dataset containing performance statistics and salaries of professional baseball players from the 1986-1987 MLB seasons.

**Features include:**
- Career and seasonal stats: `AtBat`, `Hits`, `HmRun`, `Runs`, `Walks`, etc.
- Demographic and league information: `League`, `Division`, `NewLeague`
- Target variable: `Salary` (1987 annual salary in thousands)

# Technologies Used

- R & RMarkdown
- `ggplot2`, `caret`, `nnet`, `randomForest`, `xgboost`
- Multinomial logistic regression
- LASSO regression
- Cross-validation techniques


## Data Cleaning & Preprocessing

- Removed missing values
- Standardized numerical predictors
- Created the target variable (`SalaryLevel`) : BanchWarmer, Starter, Pro, AllStar
- Vizulized data with multiple graphs 

## 🔍 Model Evaluation

To assess the effectiveness of our models, we compared:

- **Multinomial Logistic Regression**
- **Random Forest**
- **XGBoost (Tuned)**
- **LASSO Logistic Regression**

We used both:
- **Vanilla validation (80/20 split)**
- **10-Fold Cross-Validation**

### Evaluation Metrics:
- Accuracy
- Precision & Recall
- F1 Score
- Confusion Matrices (per class)
- Cross-validated classification errors

### Key Insights:
- **XGBoost** outperformed other models in raw predictive power.
- **Random Forest** balanced performance with generalizability.
- **LASSO** proved helpful in feature selection.
- **Logistic Regression** offered strong interpretability.

Misclassifications were most common between the adjacent salary levels (`Starter`, `Pro`), and class imbalance was particularly challenging for the `AllStar` group.


## Conclusion

This project highlights the importance of:

- Combining multiple models for comparison
- Evaluating performance beyond just accuracy
- Addressing class imbalance in real-world datasets

The techniques used here — from PCA and clustering to model tuning and cross-validation — provide a solid, reproducible pipeline for predictive analysis in sports data.

---


