# Building Advanced Data Models and DAX Calculations

## Construction Project Analytics Using Microsoft Power BI

### Project Overview

This project focuses on developing a structured data model and creating DAX calculations using Microsoft Power BI Desktop. It uses publicly available construction-related data from the **Zambia Electronic Projects Registry and Analytics (ZEPRA)** platform.

The purpose is to connect project, procurement and contract award information, calculate useful performance indicators and present the results through a Power BI dashboard.

### Objectives

- Import and prepare construction-related datasets using Power Query.
- Examine data quality, missing values and column data types.
- Identify primary keys and relationship fields.
- Build a structured relational data model.
- Develop DAX measures for construction and procurement analysis.
- Design a dashboard to present key indicators and project distributions.
- Identify data limitations that may affect analytical results.

### Data Sources

Three publicly available CSV datasets were used:

| Dataset | Description |
|---|---|
| Project Register | Project details, locations, budgets, status and physical completion information |
| Procurement Register | Procurement references, methods, estimated values and bid information |
| Contract Awards | Award identifiers, suppliers, contract values and award dates |

**Source:** [ZEPRA Official Website](https://zepra.co.zm/)

**Dataset download links:**

- [Project Register CSV](https://zepra.co.zm/open-data/download/projects?format=csv)
- [Procurement Register CSV](https://zepra.co.zm/open-data/download/procurement?format=csv)
- [Contract Awards CSV](https://zepra.co.zm/open-data/download/awards?format=csv)

### Tools and Technologies

- Microsoft Power BI Desktop
- Power Query Editor
- Data Analysis Expressions (DAX)
- CSV (Comma-Separated Values)
- Microsoft Word

### Data Model Design

The final Power BI model contains four tables:

1. `project_register`
2. `procurement_register`
3. `contract_awards`
4. `DimOCID`

The `DimOCID` lookup table was created using unique, non-blank OCID values from the Procurement Register.

Three active one-to-many relationships were established:

| One-side table | Many-side table | Relationship key |
|---|---|---|
| Project Register | Procurement Register | `zepra_id` → `linked_project_id` |
| DimOCID | Procurement Register | `ocid` → `ocid` |
| DimOCID | Contract Awards | `ocid` → `ocid` |

All three relationships use single-direction filtering.

### DAX Calculations

The project includes measures for:

- Total Award Amount
- Total Number of Awards
- Average Award Amount
- Average Physical Completion
- Average Bids Received
- Total Projects
- Average Schedule Delay (tested but not included in the dashboard because suitable date information was unavailable)

Four additional measures were developed to examine data completeness:

- Projects With Physical Progress
- Projects With Physical Progress %
- Awards With Recorded Amount
- Award Amount Data Coverage %

### Dashboard Overview

The Power BI dashboard contains six KPI cards and two charts.

**KPI indicators:**
- Total Projects: 930
- Total Award Amount: Approximately ZMW 93.66 billion
- Total Number of Awards: Approximately 30,000
- Average Award Amount: Approximately ZMW 3.12 million
- Average Physical Completion: 27.67%
- Average Bids Received: 1.61

**Charts:**
- Projects by Status
- Projects by Province

A separate DAX Validation page was also created to display the results of the four additional measures.

### Key Data Limitations

The analysis identified several limitations in the source datasets:

- Missing project budget information.
- Incomplete linked project identifiers.
- Limited physical completion information.
- Missing planned and actual completion dates for schedule delay analysis.
- No recorded values in the `amount_paid` field.

Missing values were retained where appropriate rather than automatically replaced with zero. These limitations were considered when interpreting the results.

### Project Deliverables

The project documentation and supporting files include:

- Power BI report (`.pbix`)
- Internship project report (`.docx`)
- Dashboard screenshot
- Data model relationship screenshot
- DAX validation screenshot

### Repository Structure

The repository is organised into the following folders:

```text
Building_Advanced_Data_Models_and_DAX/
│
├── README.md
├── report/
│   └── Building_Advanced_Data_Models_and_DAX_Calculations_Report.docx
│
├── powerbi/
│   └── Construction_Project_Analytics.pbix
│
├── screenshots/
│   ├── dashboard_overview.png
│   ├── data_model_relationships.png
│   └── dax_validation.png
│
└── data/
    └── README.md
```

*The file and folder names above are suggested names; use the actual names in your repository.*

### Conclusion

This project demonstrates how Microsoft Power BI can be used to prepare data, build relational models, develop DAX calculations and create visual reports for construction project analytics. It also highlights the importance of data quality, accurate relationships and careful interpretation when working with real-world public datasets.

### References

- [ZEPRA Official Website](https://zepra.co.zm/)
- [Microsoft Power BI Documentation](https://learn.microsoft.com/en-us/power-bi/)
- [Microsoft DAX Reference](https://learn.microsoft.com/en-us/dax/)
- [Microsoft Power Query Documentation](https://learn.microsoft.com/en-us/power-query/)
