# Hospital Operations & Discharge Delay Analyzer

An interactive Power BI dashboard designed to target, categorize, and mitigate patient discharge bottlenecks to optimize hospital Bed Turnover Rates and patient flow[cite: 1].

---

## 📊 Dashboard Preview
![Discharge Delay Dashboard](Power%20BI%20dashboard%20ss.jpg)

---

## 🎯 Key Objectives & Insights
* **Average Length of Stay (LOS):** Analyzed historical patient admission logs to calculate average hospital stay durations by ward[cite: 1].
* **Bottleneck Identification:** Pinpointed the specific operational phases causing the longest administrative delays (e.g., insurance approvals, pharmacy clearances)[cite: 1].
* **Patient Flow Patterns:** Tracked admission and discharge volumes over time to predict high-traffic seasonal periods[cite: 1].

---

## 🛠️ Tools Used
* **Power BI Desktop:** Dashboard design, custom data visualizations, and operational modeling[cite: 1].
* **Power Query (ETL):** Cleaning messy admission logs, managing column values, and transforming date variables to calculate precise length-of-stay durations[cite: 1].
* **Python (Google Colab):** Used for initial exploratory data analysis (EDA) and data wrangling.

---

## 🐍 Data Cleaning & Python Notebook
The data preprocessing steps and exploratory analysis for this dashboard were conducted in Python. 

* **View the Python Notebook:** Open and run the analysis code directly [**on Google Colab by clicking here**](Display_Discharge_Dashboard.ipynb).

---

## 📂 How to Open This Project
1. Download the `hospital_discharge_data.csv` raw dataset from this repository to view the records.
2. If you would like to run the model locally, download the `.pbix` file (once uploaded) and open it in **Power BI Desktop**[cite: 1].
