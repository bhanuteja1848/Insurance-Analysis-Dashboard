

# 🚗 Vehicle Insurance Analytics Dashboard

[![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![SQL](https://img.shields.io/badge/SQL-CC292B?style=for-the-badge&logo=microsoftsqlserver&logoColor=white)](https://en.wikipedia.org/wiki/SQL)


An interactive, end-to-end Power BI analytics solution designed to evaluate vehicle insurance policy trends, customer demographics, claims distributions, and premium revenues. This dashboard translates complex insurance data into actionable business insights for underwriting and operational strategies.

---

## 🎥 Walkthrough Video

https://github.com/user-attachments/assets/b4e5c2e0-a0b7-4d0d-83d4-6ef715294871


---

## 📊 Dashboard Pages & Data Model

### Data Model Architecture
![Data Model](Images/data%20model.png)

### Dashboard Visualizations

#### Executive Summary (Page 1)
![1st Page](Images/1st%20page.png)

####  Customer & Vehicle Demographics (Page 2)
![2nd Page](Images/2nd%20page.png)

#### Claims & Policy Deep-Dive (Page 3)

![3rd Page](Images/3rd%20page.png)

---

## 💡 Key Business Insights

- **Premium vs. Claim Ratio:** Visibility into net profit margins across different vehicle classes and coverage types.
- **Demographic Breakdown:** Customer segmentation by age group to evaluate high-risk vs. profitable profiles.
- **Claim Frequency & Severity:** Granular tracking of claims filed by monthly cohorts, identifying seasonal spikes in claim volume.

---

## 🛠️ Technical Architecture

### 1. Data Ingestion & Transformation (Power Query)
- Standardized and cleansed historical policy and claim records.
- Handled null values, formatted dates, and built custom M-Query conditional columns for age tier grouping and claim status indexing.

### 2. Data Modeling (Star Schema)
- Designed an optimized **Star Schema** with core fact tables (`fact_policy.png`) connected to dimension tables (`dim_customer.png`, `dim_vehicle.png`).
- Configured 1-to-many single-direction relationships to optimize DAX engine performance.

### 3. DAX Measures & Analytics
Calculated measures using DAX including:
- **Total Premium Revenue:** Sum of active policy premiums.
- **Total Claim Amount:** Aggregated payout values across resolved and pending claims.
- **Loss Ratio (%):** $\frac{\text{Total Claims}}{\text{Total Premiums}} \times 100$
- **YoY Growth:** Time-intelligence functions (`SAMEPERIODLASTYEAR`, `TOTALYTD`) for revenue and claim comparisons.

---

## 📁 Repository Structure

```text
Insurance-Analysis-Dashboard/
│
├── .gitattributes                # Git LFS config for tracking video/large media
├── README.md                     # Project documentation
├── Insurance Dashboard.pbix      # Main Power BI Desktop file
│
├── data/                         # Source datasets
│
└── Images/
    ├── 1st page.png              # Executive Summary View
    ├── 2nd page.png              # Claims Analysis View
    ├── 3rd page.png              # Customer Demographics View
    ├── car icon.png              # Asset icon
    ├── data model.png            # Complete Data Model Schema
    ├── dim_customer.png          # Dimension schema preview
    ├── dim_vehicle.png           # Dimension schema preview
    ├── fact_policy.png           # Fact table schema preview
    └── Project Overview Video.mp4 # Video demonstration
