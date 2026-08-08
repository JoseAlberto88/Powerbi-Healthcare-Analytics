# Healthcare Encounters. Power BI Analytics Project

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-2C5E9E?style=for-the-badge&logo=microsoft&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

A star-schema Power BI data model and dashboard suite built on a healthcare encounters dataset (1,500 patient encounters across 500 patients, 8 tables). This project demonstrates the full analytics workflow: ETL and data profiling, dimensional modeling, DAX measure design, and interactive report/dashboard development.

> Built as part of a Business Intelligence course assignment. Dataset is synthetic/course-provided, used here for demonstration purposes only.

## What this project covers

- **ETL & Data Profiling** — Imported and profiled 8 tables in Power Query (Column Quality, Column Distribution). Identified and corrected two real data quality issues:
  - A `Quarter` field mixing year and quarter into a single text value, split into a clean numeric field.
  - A `DischargeDateID` field generated via incorrect digit-based arithmetic, producing invalid calendar dates — recalculated using proper date arithmetic (`Date.AddDays`).
- **Dimensional Modeling** — Star schema with one fact table (`FactEncounter`) and seven dimension tables (Calendar, Diagnosis, Facility, Patient, Payer, Procedure, Provider), validated with a cross-table matrix visual.
- **DAX** — 13 measures spanning Math/Statistical, Counting, Logical/Conditional, `CALCULATE`, and Time Intelligence functions.
- **Visualization** — Three report pages (Financial & Operational Overview, Patient Demographics & Diagnosis Patterns, Readmissions & Quality Insights) using bar, pie, and line charts, a matrix, a table, and interactive slicers.

## Key insights

- Orthopedics drives the highest patient volume and billed charges of any specialty (~$9.3M of $36.3M total).
- Average cost per encounter is nearly identical between Clinics and Hospitals (~$24,250 vs ~$24,140), suggesting facility type alone isn't a strong cost driver.
- Overall readmission rate is ~15%; high-cost encounters (>$130,000) appear in both Clinic and Hospital settings.
- Average total cost is similar for readmitted vs. non-readmitted encounters, suggesting readmission status alone doesn't drive cost.
- Payer mix is well diversified, with no single payer type exceeding ~21% of encounters.

## Data model

![Star schema data model](screenshots/Start-Schema-Data-Model.png)

## Report pages

**Financial & Operational Overview**
![Financial overview dashboard](screenshots/Financial-Overview-Dashboard.png)

**Patient Demographics & Diagnosis Patterns**
![Patient demographics dashboard](screenshots/Patient-Demographics-Dashboard.png)

**Readmissions & Quality Insights**
![Readmissions dashboard](screenshots/Readmission-Dashboard.png)

## Tools & techniques

`Power BI` · `Power Query (M)` · `DAX` · `Star Schema Design` · `Data Profiling` · `Data Visualization`

## Repository contents

```
├── screenshots/ # Data model diagram + dashboard exports
├── docs/
│ ├── Project_Report.pdf # Full written report (ETL, model, DAX, insights)
│ └── Video_Presentation_Script.md
└── README.md

```
*Note: the `.pbix` file is not included in this repository, as it contains coursework data provided under a course license.*

## About the Author

**Jose Alberto Martinez Morales**

Master's student in Data Analytics at the University of Niagara Falls, and holder of a Master's degree in Mathematics from UNAM (Universidad Nacional Autónoma de México). Passionate about applying analytical and statistical thinking to real-world data problems, with a growing focus on business intelligence and healthcare analytics.

🔗 [LinkedIn](https://www.linkedin.com/in/josemartinez88/)

**Beyond data:** science fiction, Vietnamese culture, video games, dance machines, learning French, and following scientific topics in AI, mathematics, statistics, and physics/cosmology.