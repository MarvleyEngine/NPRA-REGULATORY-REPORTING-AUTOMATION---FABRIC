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

- <img width="1393" height="670" alt="image" src="https://github.com/user-attachments/assets/164c2608-f34e-4f96-a8ab-1c6a686c817f" />
<img width="1421" height="678" alt="image" src="https://github.com/user-attachments/assets/b5bbacba-f351-4c6b-b627-bf4a3eccd5f2" />
<img width="1470" height="627" alt="image" src="https://github.com/user-attachments/assets/4c956ad2-0db9-4c1c-a035-68e33e22bd10" />




## Error Handling
- Pipeline captures failures at ingestion or transformation stage
- Sends automated email alerts for troubleshooting
-<img width="1322" height="755" alt="image" src="https://github.com/user-attachments/assets/d1931130-2825-413e-8b24-82d0318ae8fe" />
- <img width="1417" height="751" alt="image" src="https://github.com/user-attachments/assets/a36bbc73-c27e-4984-b13a-f1e6ad25f573" />
<img width="1421" height="737" alt="image" src="https://github.com/user-attachments/assets/b7ad0997-d5f1-46e5-a952-9075541e44ab" />


## Solution Overview
Automated reporting solution built for NPRA regulatory submissions.
<img width="1412" height="770" alt="image" src="https://github.com/user-attachments/assets/bbe70961-71b9-4876-8b9c-be822d1b3843" />
<img width="1387" height="731" alt="image" src="https://github.com/user-attachments/assets/6893bb69-97ab-47af-a551-02ac9f031bc4" />

<img width="1536" height="1024" alt="ChatGPT Image May 22, 2026, 01_40_54 PM" src="https://github.com/user-attachments/assets/422c1279-c917-46a9-b6c7-13c5a41c573a" />
