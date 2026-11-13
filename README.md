# BigMart Sales: Data Cleaning, EDA and Sales Prediction

**Week 2 Assignment** | WeIntern Data Science Internship

## Objective
Clean a raw sales dataset, explore it statistically and visually, and build a machine learning model that predicts item sales.

## Dataset
BigMart Sales training data (Kaggle): 8,523 rows and 12 columns, covering 1,559 products in 10 outlets. The target is `Item_Outlet_Sales`.

## Tools and Libraries
Python, pandas, numpy, matplotlib, seaborn, scikit-learn, Jupyter Notebook (VS Code).

## Tasks and Key Results
1. **Data cleaning** (`task1_data_cleaning.ipynb`): handled 3,873 missing values (item weight and outlet size), standardised inconsistent fat-content labels, replaced 526 invalid zero visibilities, capped 144 visibility outliers, found no duplicates, encoded the categories and saved a cleaned and an encoded dataset.
2. **Exploratory analysis** (`task2_eda.ipynb`): sales depend mostly on outlet type (Type3 supermarkets average 3,694 per item against 340 for grocery stores) and item price (correlation 0.57). Product category and fat content have little effect.
3. **Sales prediction** (`task3_sales_prediction.ipynb`): compared a mean baseline, Linear Regression and Random Forest. The tuned Random Forest was best (test R² 0.612, RMSE 1,026, MAE 721). Price and relative visibility were the most important features.

## Folder Structure
```
data-science-week2-assignment/
├── data/
│   ├── raw/
│   └── cleaned/
├── notebooks/
│   ├── task1_data_cleaning.ipynb
│   ├── task2_eda.ipynb
│   └── task3_sales_prediction.ipynb
├── outputs/
│   └── charts/
├── reports/
├── screenshots/
├── README.md
└── requirements.txt
```

## Reports
- `reports/task1_cleaning_report.pdf`: Task 1 data cleaning report (decisions and before/after comparison)
- `reports/task1_notebook_export.pdf`: Task 1 notebook export
- `reports/task2_eda.pdf`: Task 2 notebook export (EDA report)
- `reports/task3_sales_prediction.pdf`: Task 3 notebook export

## How to Run
1. Install the packages: `pip install -r requirements.txt`
2. Open the notebooks in `notebooks/` in order (Task 1, then Task 2, then Task 3), because each uses the output of the one before.
3. Select **Restart**, then **Run All**. The notebooks read from `data/raw/` and `data/cleaned/` and save charts to `outputs/charts/`.

## Limitations
The dataset covers a single year with no order dates, so time-based forecasting was not possible. The model predicts sales for item-outlet combinations and not for future periods.

## Author Details
**Name:** Snehal Subhash Mali  
**Programme:** WeIntern Data Science Internship, Week 2