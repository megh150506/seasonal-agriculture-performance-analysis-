# Seasonal Agriculture Performance Analysis

**VOIS x AICTE — Data Analytics & Visualization Major Project**

## 📌 Problem Statement
Agricultural activities are influenced by seasonal variations in environmental conditions,
farming practices, resource availability and market conditions. This project analyzes a
4,000-record agricultural dataset spanning three seasons (**Kharif, Rabi, Zaid**), 8 Indian
states and 8 crops to identify meaningful seasonal patterns, trends, relationships and
differences in agricultural performance — and to turn those findings into data-driven
recommendations for seasonal agricultural planning.

## 📂 Repository Structure
```
├── data/
│   └── seasonal_agriculture_performance_dataset.csv
├── notebooks/
│   └── Seasonal_Agriculture_Performance_Analysis.ipynb   # full analysis
├── outputs/
│   └── *.png                                             # exported charts
├── requirements.txt
└── README.md
```

## 🧭 What the Notebook Covers
1. Dataset loading & exploration
2. Data cleaning (season-wise median imputation for missing values, duplicate removal)
3. Seasonal overview & summary statistics
4. Yield distribution by season (+ one-way ANOVA significance test)
5. Environmental conditions (rainfall, temperature, humidity) by season
6. Economic performance — cost, revenue, profit by season
7. Resource usage & water-use efficiency by season and irrigation method
8. Disease/pest risk distribution by season
9. Crop × Season yield heatmap
10. State × Season regional profit patterns
11. Rainfall vs. yield relationship, and a correlation matrix of key variables
12. Key findings and data-driven recommendations

## 🛠️ Tech Stack
- Python 3
- pandas, NumPy — data cleaning & aggregation
- Matplotlib, Seaborn — visualization
- SciPy — statistical testing (ANOVA)
- Jupyter Notebook

## ▶️ How to Run
```bash
git clone <this-repo-url>
cd seasonal-agriculture-performance-analysis
pip install -r requirements.txt
jupyter notebook notebooks/Seasonal_Agriculture_Performance_Analysis.ipynb
```

## 👥 End Users
- Agricultural policymakers and state agriculture departments (seasonal planning)
- Farmers and farmer cooperatives (crop-season and irrigation decisions)
- Agri-fintech and insurance providers (seasonal risk assessment)
- Agricultural researchers and students

## 🔭 Future Scope
- Extend the analysis with a predictive model (e.g., yield or profit forecasting) using
  regression/ML techniques.
- Build an interactive dashboard (Power BI / Streamlit) for real-time seasonal monitoring.
- Incorporate additional years of data to study year-over-year seasonal trends.
- Add geospatial visualization (choropleth maps) for state-level insights.

## 📄 License
This project is submitted as part of the VOIS x AICTE Data Visualization course major project.
