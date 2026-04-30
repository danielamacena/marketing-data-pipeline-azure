# marketing-data-pipeline-azure
End-to-end marketing data pipeline using Azure Data Factory, Azure SQL and Power BI, including data quality monitoring and KPI analysis.


# Marketing Data Pipeline (Azure Data Factory)

## 📌 Overview
This project simulates a real-world marketing analytics pipeline designed to ensure data reliability, business insight generation, and data quality monitoring.

---

## 🏗 Architecture

### Bronze Layer
Raw data ingestion from CSV files stored in Azure Blob Storage into Azure SQL without any transformation.

Purpose:
- Preserve original data
- Enable traceability and data lineage

---

### Silver Layer
Data cleaning and standardization.

Key transformations:
- Replaced null values (campaign_name, cost, revenue)
- Removed invalid records (e.g. zero impressions)
- Ensured data consistency

---

### Gold Layer
Business-ready dataset with calculated KPIs.

Metrics calculated:
- CTR (Click Through Rate)
- Conversion Rate
- CPA (Cost per Acquisition)
- ROAS (Return on Ad Spend)
- Profit

---

### Data Quality Layer
Identification and tracking of problematic records.

Checks implemented:
- Missing campaign names
- Zero impressions
- Conversions greater than clicks
- Missing revenue
- Zero cost

Each issue is classified and stored with a description for monitoring and debugging.

---

## 🔄 Data Flow

CSV (Azure Blob Storage)  
→ Bronze (Raw Data)  
→ Silver (Cleaned Data)  
→ Gold (Business KPIs)  
→ Data Quality (Error Monitoring)

---

## ⚙️ Technologies Used

- Azure Data Factory
- Azure SQL Database
- Azure Blob Storage
- Power BI
- Python (data simulation)

---

## 📊 Example Data Quality Issues

| Campaign | Issue |
|---------|------|
| NULL campaign name | Missing campaign name |
| impressions = 0 | Zero impressions |
| conversions > clicks | Logical inconsistency |
| revenue = NULL | Missing revenue |

---

## 💡 Key Learnings

- Designed a multi-layer data pipeline (Bronze/Silver/Gold)
- Implemented business KPI calculations
- Built data quality monitoring framework
- Ensured data reliability for decision-making
- Applied best practices in data engineering and analytics

---
## 📈 Business Impact

This pipeline ensures:
- Reliable marketing performance analysis
- Prevention of misleading KPIs
- Improved decision-making for campaign optimization

---

## 📸 Screenshots

## 📸 Pipeline Overview

![Pipeline](screenshots/pipeline-overview.png)

---

## 🚀 Next Steps

- Enhance data quality rules
- Add pipeline automation (triggers)
- Improve dashboard storytelling in Power BI
