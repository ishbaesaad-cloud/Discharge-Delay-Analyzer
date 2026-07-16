## 📌 Project Summary

Hospital discharge delays extend length of stay (LOS), reduce bed availability, and drive up operating costs. This project analyzes a 500-record synthetic hospital discharge dataset to identify **where** delays happen, **how long** they last, and **which operational phase** is most responsible — turning raw admission/discharge logs into an actionable Power BI dashboard for hospital operations teams.

**Key finding:** [INSERT: e.g., "Pharmacy clearance accounted for 34% of total discharge delay time, more than any other single phase, concentrated in the Cardiology and Orthopedics wards."]

**Business impact:** [INSERT: e.g., "Reducing pharmacy clearance delay by even 1 hour per patient could free up an estimated X bed-days per month."]

---

## 📊 Dashboard Preview

![Discharge Delay Dashboard](power_bi_dashboard_screenshot.jpg)

**➡️ [Open the interactive Power BI dashboard file](discharge_delay_dashboard.pbix)** *(requires Power BI Desktop — free download from Microsoft)*

---

## 🎯 Key Objectives & Insights

- **Average Length of Stay (LOS) by Ward** — Calculated average and median LOS across hospital wards to flag which departments run longest. [INSERT: top 1-2 wards by LOS, with numbers]
- **Bottleneck Identification** — Isolated the specific administrative phases (insurance approval, pharmacy clearance, physician sign-off, transport/bed assignment) contributing the most delay time. [INSERT: ranked list with % or hours]
- **Patient Flow Patterns** — Tracked admission/discharge volume over time to identify high-traffic periods and staffing mismatches. [INSERT: e.g., "Discharge volume peaks on Mondays and drops 40% on weekends despite steady admission rates."]
- **Recommendation(s)** — [INSERT: your staffing/scheduling recommendation(s) derived from the data — this is the part that shows analytical judgment, not just reporting]

---

## 🛠️ Tools & Methods

| Tool | Purpose |
|---|---|
| **Python (Pandas, Matplotlib)** | Data cleaning, exploratory data analysis, and initial visualization in Google Colab |
| **ReportLab** | Automated PDF summary report generation |
| **Power BI Desktop** | Interactive dashboard design and DAX-based KPI calculations |
| **Power Query (M)** | ETL — cleaning messy admission logs, standardizing date/time fields, calculating LOS |

---

## 🐍 Python Notebook (EDA & Data Cleaning)

Data preprocessing and exploratory analysis were done in Python before being loaded into Power BI.

**➡️ [View the notebook](discharge_delay_analysis.ipynb)** *(or [open directly in Google Colab](https://colab.research.google.com/github/ishbaesaad-cloud/Discharge-Delay-Analyzer/blob/main/discharge_delay_analysis.ipynb))*

What it covers:
- Loading and cleaning the raw discharge log dataset
- Handling missing/inconsistent date-time values
- Calculating length-of-stay and delay-phase durations
- Exploratory visualizations (4 charts: [INSERT: name them, e.g., "LOS by ward", "delay phase breakdown", "admissions over time", "delay distribution histogram"])
- Exporting a summary PDF report via ReportLab

---

## 📂 Repository Structure

```
Discharge-Delay-Analyzer/
├── discharge_delay_analysis.ipynb     # Python EDA & data cleaning notebook
├── discharge_delay_dashboard.pbix     # Power BI dashboard file
├── hospital_discharge_data.csv        # Raw synthetic dataset (500 records)
├── power_bi_dashboard_screenshot.jpg  # Dashboard preview image
├── requirements.txt                   # Python dependencies
├── LICENSE
└── README.md
```

---

## 🚀 How to Run This Project

1. **Clone the repo:**
   ```bash
   git clone https://github.com/ishbaesaad-cloud/Discharge-Delay-Analyzer.git
   ```
2. **Explore the data:** Open `hospital_discharge_data.csv` directly, or run the notebook:
   ```bash
   pip install -r requirements.txt
   ```
   then open `discharge_delay_analysis.ipynb` in Jupyter or Google Colab.
3. **View the dashboard:** Open `discharge_delay_dashboard.pbix` in [Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494).
