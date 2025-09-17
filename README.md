# 📊 Linear Regression on Boston Housing Dataset

This project demonstrates **Simple Linear Regression (SLR)** and **Multiple Linear Regression (MLR)** using the **Boston Housing dataset**.  
It covers data preprocessing, model implementation, assumption checks, and report generation (Word/PDF with plots and tables).

---

## 📂 Dataset

- File: `Boston.csv`  
- Rows: 506  
- Columns: 14 (features) + 1 target (`medv`: Median value of owner-occupied homes)

**Key variables:**
- `crim` – Per capita crime rate by town  
- `rm` – Average number of rooms per dwelling  
- `lstat` – % lower status of the population  
- `ptratio` – Pupil-teacher ratio by town  
- `medv` – Median house value (**target**)  

---

## ⚙️ Steps Implemented

### 1. Data Preprocessing
- Loaded dataset using `pandas`  
- Checked dataset shape and missing values  
- Performed correlation analysis to find top predictors  

### 2. Simple Linear Regression (SLR)
- Predictor: `lstat` (highest correlation with `medv`)  
- Fitted model:  
  \[
  \hat{y} = \beta_0 + \beta_1 \cdot lstat
  \]  
- Residual analysis: residual vs fitted plot and QQ plot  
- R² ≈ **0.54** → `lstat` explains ~54% of variance in house prices  

### 3. Multiple Linear Regression (MLR)
- Predictors: All features except `medv`  
- Model equation:  
  \[
  \hat{y} = \beta_0 + \beta_1 \cdot x_1 + \beta_2 \cdot x_2 + \dots + \beta_p \cdot x_p
  \]  
- Performance: R² ≈ **0.74**, Adjusted R² ≈ **0.73**  
- Coefficients saved in a summary table  

### 4. Assumption Checks
- **Linearity**: Checked via residual plots  
- **Normality**: Verified with QQ plot  
- **Homoscedasticity**: Checked with residual vs fitted values plot  
- **Multicollinearity**: Variance Inflation Factor (VIF) analysis  

### 5. Report Generation
- Generated automated report with:
  - Dataset sample  
  - Correlation table and heatmap  
  - Regression results and metrics  
  - Residual diagnostics  
  - VIF analysis table  
- Exported to **Word (`.docx`)** and/or **PDF**  

---

## 📈 Results Summary

| Model | R² | Adjusted R² | Key Notes |
|-------|----|-------------|-----------|
| SLR (lstat) | ~0.54 | - | Captures ~54% variance, residuals show non-linearity |
| MLR (all features) | ~0.74 | ~0.73 | Stronger fit, but multicollinearity present |

---

## 🛠️ Requirements

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn statsmodels python-docx
