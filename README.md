# Advanced_Construction_Data_Modeling
This project uses Microsoft Power BI to analyse construction project, procurement and contract award information from the Zambia Electronic Projects Registry and Analytics (ZEPRA).
# Building Advanced Data Models and DAX Calculations

## Project Overview

This project uses Microsoft Power BI to analyse construction project, procurement and contract award information from the Zambia Electronic Projects Registry and Analytics (ZEPRA).

The objective is to prepare multiple datasets, develop a relational data model, create DAX measures and present important results through an interactive dashboard.

## Objectives

- Import and transform construction-related datasets.
- Inspect data quality and handle missing values.
- Develop a relational data model.
- Create DAX measures for important KPIs.
- Build a Power BI dashboard for project analysis.
- Identify data limitations and possible improvements.

## Datasets

Three public CSV datasets were used:

1. Project Register
2. Procurement Register
3. Contract Awards

**Data source:** [ZEPRA Official Website](https://zepra.co.zm/)

## Tools and Technologies

- Microsoft Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- CSV datasets
- Microsoft Word

## Data Model

The final model contains four tables:

- `project_register`
- `procurement_register`
- `contract_awards`
- `DimOCID`

Three active one-to-many relationships were created using project identifiers and OCID values.

## Key Performance Indicators

The dashboard includes:

- Total Projects: 930
- Total Award Amount: Approximately ZMW 93.66 billion
- Total Number of Awards: Approximately 30 thousand
- Average Award Amount: Approximately ZMW 3.12 million
- Average Physical Completion: 27.67%
- Average Bids Received: 1.61

## Dashboard Visualisations

- Projects by Status
- Projects by Province
- KPI cards for project, award and procurement indicators

## Project Structure

```text
Advanced_Construction_Data_Modeling/
│
├── data/
│   ├── project_register.csv
│   ├── procurement_register.csv
│   └── contract_awards.csv
│
├── screenshots/
│   ├── dashboard_overview.png
│   └── data_model_relationships.png
│
├── report/
│   └── Building_Advanced_Data_Models_and_DAX_Calculations_Report.docx
│
├── README.md
└── .gitignore
```

## Limitations

Some source fields contain missing information, including budget values, linked project identifiers and completion dates. Therefore, certain financial and schedule calculations could not be completed reliably.

The dashboard presents results based on the available records and should be interpreted with these limitations in mind.

## Author

Student Project — Power BI Data Analytics Internship
