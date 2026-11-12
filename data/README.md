# Dataset Documentation

## Overview

This folder contains the three original CSV datasets used in the Power BI project, Building Advanced Data Models and DAX Calculations.

The datasets were obtained from the Zambia Electronic Projects Registry and Analytics (ZEPRA) public open-data portal.

## Dataset Files

### 1. project_register.csv

Contains construction and infrastructure project information, including project identifiers, titles, sectors, locations, project status, budget information and physical completion details.

### 2. procurement_register.csv

Contains procurement-related information, including procurement identifiers, OCIDs, procuring entities, procurement methods, estimated values, publication dates and bid information.

### 3. contract_awards.csv

Contains contract award information, including award identifiers, suppliers, contract values, award dates, contract status and related procurement references.

## Data Sources

- Project Register: https://zepra.co.zm/open-data/download/projects?format=csv
- Procurement Register: https://zepra.co.zm/open-data/download/procurement?format=csv
- Contract Awards: https://zepra.co.zm/open-data/download/awards?format=csv
- Official website: https://zepra.co.zm/

## Data Preparation

The CSV files were imported into Power BI Desktop. Data inspection, profiling, data type transformations and identifier validation were performed using Power Query Editor.

The original source files are included here for reference and reproducibility. Data preparation was carried out inside Power BI.

## Important Note

Some source columns contain missing values. These values were not automatically replaced with zero because missing information does not necessarily mean a value of zero.
