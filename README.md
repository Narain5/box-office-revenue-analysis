# 🎬 Box Office Revenue Analysis & Prediction

An end-to-end **Data Analysis and Machine Learning** project that explores **box office revenue patterns** and builds predictive models using movie metadata such as budget, popularity, runtime, release timing, and production companies.

---

## 📌 Project Overview

This project focuses on answering two key questions:

1. **What factors influence box office revenue?**
2. **Can we build baseline machine learning models to predict movie revenue?**

The project includes:
- Data cleaning & preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Predictive modeling
- Model evaluation

---

## ✨ Key Highlights

- Cleaned and processed real-world movie metadata
- Visualized:
  - Top-grossing movies
  - Movies released per year
  - Monthly and weekday release trends
  - Return on Investment (ROI)
  - Budget vs Revenue (log-scaled)
  - Correlation heatmap
- Engineered meaningful features from dates and numeric fields
- Trained and evaluated baseline ML models:
  - Linear Regression
  - Random Forest Regressor
- Evaluated using **R² Score** and **RMSE**

---

---

## 🗃️ Dataset Description

The dataset contains movie-level metadata such as:

- `title`
- `budget`
- `revenue`
- `popularity`
- `runtime`
- `release_date`
- `production_companies`

> ⚠️ Note:  
> If the full dataset is large or copyrighted, it is recommended to:
> - Upload only a **sample dataset**
> - Or provide instructions to download the dataset separately and place it inside the `data/` folder

---

## 🔍 Exploratory Data Analysis (EDA)

The notebook explores:

- **Top 5 highest revenue movies**
- **Number of movies released per year**
- **Monthly release trends (1921–2017)**
- **Movies released by day of week**
- **Top movies by ROI (Return on Investment)**

ROI Formula:
ROI = (revenue - budget) / budget

---

## 🧱 Feature Engineering

### Date-Based Features
- Converted `release_date` to datetime
- Extracted:
  - `release_year`
  - `release_month`
  - `release_season` (Winter, Spring, Summer, Fall)
- Created:
  - `movie_age = current_year - release_year`

### Log Transformations
Used to reduce skewness:
log_budget  = log1p(budget)
log_revenue = log1p(revenue)

### Categorical Encoding
- Label encoded `production_companies`

---

## 🤖 Machine Learning Models

### Models Implemented
- **Linear Regression**
- **Random Forest Regressor** (`n_estimators = 100`)

### Target Variable
- `revenue`

### Evaluation Metrics
- **R² Score**
- **Root Mean Squared Error (RMSE)**

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

---

## ▶️ How to Run the Project

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/box-office-revenue-analysis.git
cd box-office-revenue-analysis

python -m venv venv
source venv/bin/activate      # macOS/Linux
# venv\Scripts\activate       # Windows

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

jupyter notebook

notebooks/Box_Office_Revenue_Analysis.ipynb

📈 Observations & Insights
	•	Box office revenue and budget are highly skewed
	•	Log transformations significantly improve linear relationships
	•	Budget strongly correlates with revenue, but popularity and timing also matter
	•	Random Forest generally performs better than linear models (dataset-dependent)

⸻

🚀 Future Improvements
	•	Add more predictive features:
	•	Genres
	•	Cast size
	•	Director
	•	Ratings
	•	Language
	•	Use advanced encoding for categorical variables
	•	Apply cross-validation and time-aware splits
	•	Try advanced models (XGBoost, LightGBM)
	•	Predict log_revenue and reverse-transform predictions
	•	Build an end-to-end ML pipeline using sklearn.Pipeline

⸻

👨‍💻 Author

Narain Sarathy Jawahar
MS in Data Science
Aspiring Data Scientist | Machine Learning | Analytics | Visualization
