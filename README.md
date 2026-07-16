# Hospital Discharge Delay Analyzer

**Identifying and quantifying operational bottlenecks in patient discharge to improve hospital bed turnover and patient flow.**

---

## 📌 Project Summary

Hospital discharge delays extend length of stay (LOS), reduce bed availability, and drive up operating costs. This project analyzes a 500-patient hospital discharge dataset (Jan–Jun 2024) to identify **where** delays happen, **how long** they last, and **which operational phase** is most responsible — turning raw admission/discharge logs into an actionable Power BI dashboard for hospital operations teams.

**Key finding:** Family/Social delay reasons (e.g., waiting on family pickup or post-discharge arrangements) accounted for the largest share of total delay time — 27.2% of all discharge-delay minutes — despite Pharmacy clearance being the single most frequent delay category (25.2% of cases). Family/Social delays averaged 144 minutes per incident, nearly double the average delay length of any other category.

**Business impact:** Across the 500-patient, 6-month sample, discharge delays totaled roughly 794 hours (33 bed-days). Family/Social delays alone accounted for ~216 of those hours. Cutting Family/Social delay time in half would free up an estimated 4.5 bed-days over the same period — capacity that could be reallocated to new admissions without adding beds.

---

## 📊 Dashboard Preview

<img width="1357" height="551" alt="Power BI dashboard ss" src="https://github.com/user-attachments/assets/066dd660-c7f7-47dc-8943-45d2118408ac" />

**➡️ [Download the Power BI file](discharge_delay_dashboard.pbix)** *(requires Power BI Desktop — free download from Microsoft)*

---

## 🎯 Key Objectives & Insights

- **Average Length of Stay (LOS) by Ward** — Gynecology (8.9 days) and Surgical (8.6 days) had the longest average length of stay, while Pediatrics (7.8 days) and Cardiology (7.8 days) had the shortest.

- **Bottleneck Identification** — Ranked by total delay minutes contributed:
  1. **Family/Social** — 27.2% of total delay time (avg 144 min/case)
  2. **Pharmacy** — 22.1% of total delay time (avg 84 min/case, most *frequent* category overall)
  3. **Transport** — 18.7% of total delay time (avg 102 min/case)
  4. **Bed Management** — 14.6% of total delay time (avg 101 min/case)
  5. **Documentation** — 12.6% of total delay time (avg 65 min/case)
  6. **Physician Availability** — 4.9% of total delay time (avg 67 min/case)

- **Patient Flow Patterns** — Discharge volume was highest on Sundays (111 discharges, 22% of all cases) and lowest on Mondays (54 discharges). Weekend discharges also took longer on average — 112 minutes of delay vs. 86 minutes on weekdays — a 30% gap suggesting reduced weekend staffing (pharmacy, transport, admin) for discharge-related tasks.

- **Recommendations:**
  1. Shift discharge-coordination and social-work staffing to be weekend-weighted, since Sunday carries the highest discharge volume yet the highest average delay — the opposite of what current staffing likely supports.
  2. Prioritize a Family/Social discharge-planning workflow (e.g., earlier family notification, pre-discharge checklists) since it drives the largest share of total delay time despite not being the most frequent category — a "long-tail" problem, not a volume problem.
  3. Investigate the Medical and Pediatrics wards specifically for Family/Social delay reduction — these two ward/category combinations account for the single largest chunks of total delay minutes in the dataset.

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

**➡️ [View the notebook](Display_Discharge_DashBoard.ipynb)**

What it covers:
- Loading and cleaning the raw discharge log dataset
- Handling missing/inconsistent date-time values
- Calculating length-of-stay and delay-phase durations
- Exploratory visualizations:
  1. Average Length of Stay by Ward
  2. Delay Minutes by Category (share of total delay time)
  3. Discharge Volume by Day of Week
  4. Delay Severity Distribution (Minor / Moderate / Severe)
- Exporting a summary PDF report via ReportLab

---

## 📂 Repository Structure

```
Discharge-Delay-Analyzer/
├── Display_Discharge_DashBoard.ipynb   # Python EDA & data cleaning notebook
├── discharge_delay_dashboard.pbix      # Power BI dashboard file
├── hospital_discharge_data.csv         # Raw dataset (500 records)
├── power_bi_dashboard_screenshot.jpg   # Dashboard preview image
├── requirements.txt                    # Python dependencies
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
   then open `Display_Discharge_DashBoard.ipynb` in Jupyter or Google Colab.
3. **View the dashboard:** Open `discharge_delay_dashboard.pbix` in [Power BI Desktop](https://www.microsoft.com/en-us/download/details.aspx?id=58494) (free).

---

