# 🚗 Uber Rides Data Analysis

A comprehensive exploratory data analysis (EDA) of Uber ride data to uncover patterns in ride categories, trip purposes, time-of-day trends, and distance distributions using Python.

---

## 📌 Project Overview

This project analyzes a dataset of 1,156 Uber trips to extract meaningful business insights about ride behavior — including when people book rides, for what purpose, and how far they travel. It covers the full data analysis pipeline: data cleaning, preprocessing, feature engineering, and visualization.

---

## 📊 Dataset Description

- **Source:** [Kaggle - Uber Rides Dataset](https://www.kaggle.com/datasets/zusmani/uberdrives)
- **Size:** 1,156 rows × 7 columns

| Column | Description |
|--------|-------------|
| `CATEGORY` | Type of ride — Business or Personal |
| `START_DATE` | Start date and time of the trip |
| `END_DATE` | End date and time of the trip |
| `START` | Starting location |
| `STOP` | Destination location |
| `MILES` | Distance of the trip in miles |
| `PURPOSE` | Purpose of the ride (Meeting, Meal, etc.) |

---

## 🛠️ Libraries Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, and manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting and visualizations |
| `seaborn` | Statistical visualizations and heatmaps |
| `sklearn` | OneHotEncoding for categorical features |

---

## ⚙️ Data Preprocessing Steps

- Filled missing values in `PURPOSE` column with `"NOT"`
- Converted `START_DATE` and `END_DATE` to datetime format
- Extracted `date`, `time`, `DAY`, and `MONTH` from `START_DATE`
- Binned hours into time-of-day categories: Morning, Afternoon, Evening, Night
- Removed null rows and duplicate entries
- Applied OneHotEncoding on `CATEGORY` and `PURPOSE` columns

---

## 📈 Analysis & Visualizations

1. **Ride Category and Purpose Distribution** — Countplots comparing Business vs Personal rides across different purposes
2. **Time-of-Day Analysis** — Distribution of rides across Morning, Afternoon, Evening, and Night
3. **Category vs Purpose Breakdown** — Countplot showing which purposes are more common for Business vs Personal rides
4. **Correlation Heatmap** — Numerical feature correlation using seaborn heatmap
5. **Monthly Ride Trends** — Line plot comparing total ride counts and maximum miles per month
6. **Day-of-Week Analysis** — Bar plot showing ride frequency across days of the week
7. **Miles Distribution** — Boxplot and histogram with KDE to analyze trip distance distribution

---

## 🔍 Key Insights

- **Business rides dominate** — the vast majority of all trips are categorized as Business
- **Meetings and Meal/Entertainment** account for the highest ride volumes by purpose
- **Afternoon (10 AM – 5 PM)** is the peak booking window, suggesting strong corporate usage
- **Seasonal dip in Nov–Jan** aligns with winter months in Fort Pierce, Florida
- **Friday is the busiest day**, likely due to end-of-week meetings and client visits
- **Median trip distance is 4–5 miles**, indicating short urban commutes dominate

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/aditya2005kumar03/Uber-rides-analysis.git
cd Uber-rides-analysis
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Open the notebook:
```bash
jupyter notebook uber_analysis.ipynb
```
