# Project: ETL pipeline with Apache Hop

## Description:
The objective of this project is to construct robust data pipelines using Apache Hop, designed to facilitate continuous data flow essential for maintaining the requested dashboards. 
This initiative ensures real-time data availability and supports dynamic business intelligence needs.

## Data (not published):
Data sources are not disclosed in this repository. 
Provided are metadata in XLSX format from the client and operational data in XML format, derived from web scraping activities.

## Data Pipelines:

#### 1. Metadata pipeline:

The input process for multiple tables involves uploading Excel files, cleaning and organizing data such as removing duplicates, sorting, and adding unique identifiers like function_id and sector_id. These tables—functions, functions_sectors, companies_sectors, and companies—are then processed to ensure relevant columns are selected and any null entries are filtered out before being inserted into the Azure database. This systematic approach enhances data integrity and usability in the database by standardizing data entries and linking them appropriately across various dimensions such as sector and function.

![metadata](https://github.com/vandik-23/ETL-ApacheHOP/blob/main/metadata_pipeline.png)
   
#### 2. Operational data pipeline:

The operational pipeline is divided into two main parts, each aimed at creating specific data visualizations. The first part focuses on generating a data table and visualization that quantifies the duration jobs remain open by processing operational data, calculating the number of weeks from the provided dates, and saving the results in an Azure Database. 
The second part aims to visualize the distribution of job vacancies across different sectors by integrating data from multiple sources, assigning new sector IDs to new companies, and summarizing job counts by sector, which is then stored in the database, while also updating the jobs table with new job entries.

![operationaldata](https://github.com/vandik-23/ETL-ApacheHOP/blob/main/operational_pipeline.png)
