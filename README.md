📺 #CodeAlpha – Sales Prediction with Machine Learning
Task 4 of the CodeAlpha Data Science Internship.

📌 #Objective
Build a regression model to predict product sales based on advertising spend across three channels — TV, Radio, and Newspaper — and identify which channels actually drive sales to support marketing budget decisions.

📊 #Dataset
File: Advertising.csv
Samples: 200 records
Features (3): TV, Radio, Newspaper (advertising budgets)
Target: Sales (units sold)
Cleaning: dropped the unnecessary index column (Unnamed: 0), verified there were no missing values
🛠️ Tools & Libraries
Python
Pandas (data handling)
Matplotlib, Seaborn (visualization)
Scikit-learn (Linear Regression, train/test split, metrics)

🔄 #Workflow
Load & clean the data — removed the index column, checked for missing values
Explore — correlation heatmap + scatter plot of TV spend vs Sales
Split data 80/20 into train and test sets
Train a Linear Regression model
Evaluate using R² score and MAE
Interpret coefficients to quantify each channel's effect on sales

📈 #Results
Metric	Score
Model	Linear Regression
R² score	0.899 (explains ~90% of sales variation)
MAE	1.461
Correlation with Sales:

Channel	Correlation
TV	0.78 (strong)
Radio	0.58 (moderate)
Newspaper	0.23 (weak)
Effect on Sales (regression coefficients):

Channel	Sales increase per unit spent
Radio	0.1892
TV	0.0447
Newspaper	0.0028 (nearly zero)

🔍 #Key Insights
TV has the strongest overall correlation with sales (0.78) and drives most of the sales volume.
Radio has the highest per-unit return (0.189) — each unit spent on radio yields the biggest sales boost.
Newspaper spend has almost no effect on sales (coefficient ≈ 0.003).

✅ #Business recommendation: reallocate the Newspaper advertising budget to TV and Radio for maximum sales impact.
📁 Project Structure
CodeAlpha_SalesPrediction/├── Sales_Prediction.ipynb      # full code + outputs├── corr.png                    # correlation heatmap├── tv_sales.png                # TV spend vs Sales scatter├── actual_vs_pred.png          # actual vs predicted sales└── README.md

▶️ How to #Run
Open the notebook in Google Colab or Jupyter and run all cells. Make sure Advertising.csv is in the same folder (upload it first in Colab).
