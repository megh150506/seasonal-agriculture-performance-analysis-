🌾 Seasonal Agriculture Performance Analysis

VOIS x AICTE — Data Analytics & Visualization Major Project

An end-to-end exploratory data analysis of 4,000 farm records across three Indian growing seasons — Kharif, Rabi and Zaid — to identify statistically-backed seasonal patterns in yield, profitability, resource use and risk, and to turn those patterns into data-driven recommendations for seasonal agricultural planning.

📌 Problem Statement

Agricultural activities are influenced by seasonal variations in environmental conditions, farming practices, resource availability and market conditions. As a result, agricultural performance may differ from one season to another. Raw agricultural data does not, on its own, explain how performance changes across seasons or what patterns drive that change. This project analyzes the dataset to investigate seasonal differences in agricultural performance by identifying meaningful patterns, trends, relationships and variations.

📂 Repository Structure
├── data/
│   └── seasonal_agriculture_performance_dataset.csv   # 4,000 records, 28 columns
├── notebooks/
│   └── Seasonal_Agriculture_Performance_Analysis.ipynb  # full analysis, pre-executed
├── outputs/
│   └── 01_...10_....png                                 # exported charts
├── requirements.txt
├── .gitignore
└── README.md
🔎 Dataset at a Glance
	
Records	4,000 farms
States	8 (Andhra Pradesh, Maharashtra, Telangana, Karnataka, Gujarat, Tamil Nadu, Punjab, Madhya Pradesh)
Crops	8 (Wheat, Maize, Pulses, Rice, Cotton, Chilli, Groundnut, Sugarcane)
Seasons	Kharif, Rabi, Zaid
Irrigation methods	Drip, Flood, Rainfed, Sprinkler
Columns	28 — environmental, resource-use, yield and economic variables
Missing values	120 (in Rainfall, Soil Moisture, Yield) — cleaned via season-wise median imputation
🧭 Analysis Workflow (Notebook)
Data loading & exploration
Data cleaning — season-wise median imputation, duplicate removal
Seasonal overview & summary statistics
Yield distribution by season + one-way ANOVA
Environmental conditions (rainfall, temperature, humidity) by season
Economic performance — cost, revenue, profit by season + ANOVA
Resource usage & water-use efficiency by season and irrigation method
Disease/pest risk by season + ANOVA
Crop × Season yield heatmap
State × Season regional profit patterns
Rainfall–yield relationship & correlation matrix of key variables
Key findings and data-driven recommendations
📊 Key Results

(all numbers below are actual computed output from the executed notebook, not estimates)

Metric	Kharif	Rabi	Zaid
Farm records	1,779	1,627	594
Avg. Yield (t/ha)	5.63	5.04	4.64
Avg. Profit (₹)	178,915	87,689	-24,805
Avg. Disease/Pest Risk (%)	54.5	40.5	38.2
Avg. Rainfall (mm)	852	436	299

Statistical tests (one-way ANOVA across seasons):

Variable	F-statistic	p-value	Significant?
Yield	1.55	0.2116	❌ No
Profit	34.29	1.7 × 10⁻¹⁵	✅ Yes
Disease/Pest Risk	1049.47	≈ 0	✅ Yes
Findings
Yield is fairly stable across seasons — the difference is not statistically significant (p > 0.05).
Profit differs sharply and significantly by season, even though yield doesn't — Kharif is by far the most profitable, and Zaid runs a net average loss. Cost and market price, not yield, drive seasonal profitability here.
Disease/pest risk is significantly higher in Kharif, consistent with its higher rainfall and humidity.
Water-use efficiency does not simply favor Drip irrigation — Rainfed plots show the highest average efficiency in this dataset, ahead of Drip, Sprinkler and Flood — a counter-intuitive result worth further investigation.
Every crop yields best in Kharif and weakest in Zaid; Sugarcane outyields all other crops by an order of magnitude in every season.
Kharif is the most profitable season in 7 of 8 states — Punjab is the one exception, where Rabi is more profitable.
Most environmental variables correlate weakly with yield/profit individually, suggesting performance is driven by a combination of season, crop, cost and price rather than any single environmental factor.
Sample Visualizations
	
Show Image	Show Image
Show Image	Show Image

(all 10 charts are in /outputs and generated live inside the notebook)

💡 Recommendations
Don't rely on yield alone when planning seasons — factor in season-specific cost and market price, since Zaid's yield is only slightly lower than Kharif's but its profit is negative on average.
Step up disease/pest monitoring and preventive spend specifically in Kharif, where risk is highest.
Re-examine the irrigation-method assumption — investigate whether Rainfed's efficiency edge is a true irrigation effect or reflects which crops/regions use rainfed farming, before recommending a blanket switch to Drip.
Investigate Punjab's Rabi-favoring pattern specifically, since it diverges from the Kharif-dominant trend seen in every other state.
Prioritize Kharif-season investment and credit access for farmers, given it is the most profitable season in the large majority of states studied.
🛠️ Tech Stack
Python 3
Pandas / NumPy — data cleaning & aggregation
Matplotlib / Seaborn — visualization
SciPy — hypothesis testing (one-way ANOVA)
Jupyter Notebook — analysis & documentation
Git / GitHub — version control & hosting
▶️ How to Run
bash
git clone https://github.com/megh150506/seasonal-agriculture-performance-analysis-.git
cd seasonal-agriculture-performance-analysis-
pip install -r requirements.txt
jupyter notebook notebooks/Seasonal_Agriculture_Performance_Analysis.ipynb
👥 End Users
Agricultural policymakers & state agriculture departments — evidence-based seasonal planning
Farmers & farmer cooperatives — crop, irrigation and season selection
Agricultural researchers & academic institutions — seasonal performance studies
Agri-fintech, insurance & lending providers — seasonal risk assessment
Agri-tech startups — crop advisory & decision-support tools
🔭 Future Scope
Predictive modeling (regression/ML) for yield & profit forecasting
Interactive dashboard (Power BI / Streamlit) for real-time seasonal monitoring
Multi-year data to study year-over-year seasonal trends
Geospatial (choropleth map) visualization for state-level insights
📄 License

Submitted as part of the VOIS x AICTE Data Visualization course major project (Batch 1, 2026–2027).
