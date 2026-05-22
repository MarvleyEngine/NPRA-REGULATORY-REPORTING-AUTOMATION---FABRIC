# NPRA Monthly Regulatory Reporting Automation (Microsoft Fabric)

## Overview
This project automates the monthly regulatory reporting process for NPRA using Microsoft Fabric. It ingests large monthly datasets, transforms them, stores structured outputs, and supports reporting via SQL views and warehouse queries.
<img width="1536" height="1024" alt="ChatGPT Image May 22, 2026, 01_44_59 PM" src="https://github.com/user-attachments/assets/3ad83a1e-724a-441b-b0aa-99805fe4bbf8" />


## Architecture Flow
1. **Data Ingestion**
   - Monthly files (80–110MB) are received from BTS and placed in a shared folder.
   - Files are moved into a Fabric Lakehouse for processing.

2. **Data Transformation**
   - A Fabric Notebook performs data cleaning, validation, and transformation.

3. **Data Storage**
   - Transformed data is written into a Fabric Warehouse for structured querying.

4. **Reporting Layer**
   - Predefined SQL views are created for reporting needs.
   - Query the warehouse directly to extract regulatory report data.

5. **Automation & Notifications**
   - Pipeline sends email notifications upon:
     - Successful completion
     - Failure or error during processing

## Folder Structure
```
/NPRA-Automation
│
├── notebooks/
│   └── transform_data.ipynb
│
├── sql/
│   └── views.sql
│
├── pipeline/
│   └── fabric_pipeline_definition.json
│
├── docs/
│   └── architecture.png
│
└── README.md
```

## Key Technologies
- Microsoft Fabric (Lakehouse, Warehouse, Pipelines)
- Python (Notebook transformations)
- SQL (Warehouse views)
- Shared Folder ingestion
- Email notification system

## Output
- Clean regulatory datasets
- Query-ready warehouse tables
- Automated monthly reporting pipeline

## Error Handling
- Pipeline captures failures at ingestion or transformation stage
- Sends automated email alerts for troubleshooting

## Author
Automated reporting solution built for NPRA regulatory submissions.

<img width="1536" height="1024" alt="ChatGPT Image May 22, 2026, 01_40_54 PM" src="https://github.com/user-attachments/assets/422c1279-c917-46a9-b6c7-13c5a41c573a" />
