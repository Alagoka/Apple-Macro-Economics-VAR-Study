# Oil Price Impact Analysis on Apple Inc. (1992-2026) | Vector Autoregression (VAR) Econometric Model
Apple Inc. Financial Dynamics & Macroeconomic Volatility (1992–2026)
A Multivariate Time-Series Analysis using VAR & ARIMA
📊 Project Overview
This research quantifies the long-term relationship between global macroeconomic indicators—specifically WTI Crude Oil Prices and Real GDP Growth—and the financial performance (Net Income) of Apple Inc. over a 34-year period.
The study determines the elasticity of corporate earnings relative to energy shocks and global economic shifts, providing a robust framework for equity analysis and risk management.
🛠️ The Tech Stack
Econometric Modeling: EViews 14 (VAR, VECM, ARIMA, Cointegration Analysis).
Data Engineering: Python 3.x (Pandas, NumPy) for data cleaning, alignment, and stationarity transformations.
Environment: Jupyter Lab & GitHub Desktop.
Visualization: EViews Endogenous Graphs and Matplotlib.
🧬 Data Pipeline & Quality Control
Unlike standard financial reports, this project utilizes a custom-built Python cleaning pipeline to ensure data integrity before modeling:
Ingestion: Aggregated raw annual data from the World Bank (GDP), FRED (Oil), and SEC EDGAR (Apple 10-K filings).
Cleaning: Used Pandas to handle missing values and align disparate time-series frequencies into a unified annual dataset (1992–2026).
Feature Engineering: Applied log-transformations and first-differencing in Python to stabilize variance and prepare for stationarity testing.
Integrity Check: Validated data consistency and timeliness to ensure the model satisfies the assumptions of Vector Autoregression.
📈 Econometric Methodology
To move beyond simple correlation, I implemented a rigorous three-stage modeling process:
Unit Root Testing
Conducted Augmented Dickey-Fuller (ADF) tests to determine the order of integration for all variables, ensuring the VAR system is not spurious.
Model Estimation (VAR)Estimated an Unrestricted Vector Autoregression (VAR) model to capture the linear interdependencies among $Net\_Income$, $Oil\_Price$, and $GDP\_Growth$.
Stability & Diagnostics
Verified the model's reliability using the Inverse Roots of the AR Characteristic Polynomial. All roots lie within the unit circle, confirming the system is asymptotically stable.
🖼️ Key Findings & Visuals
System Stability (AR Roots)
The stability of the VAR system ensures that the Impulse Response Functions and Variance Decompositions are valid for forecasting.
Impulse Response Analysis
The IRF analysis reveals that Apple’s Net Income shows higher resilience to transitory oil price shocks compared to sustained shifts in global GDP growth.
📂 Repository Structure
/data: Contains the cleaned macro_data_master.csv.
/data_source: Documentation of data lineage and official sources.
/models: The functional EViews workfile (apple_macro_analysis.wf1).
/scripts: Python notebooks used for data wrangling and stationarity prep.
/results: High-resolution PNGs of stability tests and IRFs.
🚀 How to Reproduce
Clone the repository: git clone https://github.com/ALAGOKA/Apple-Macro-Econometrics-VAR-Study.git
Open models/apple_macro_analysis.wf1 in EViews 14 to inspect the VAR equations and lag-length selection criteria.
License
