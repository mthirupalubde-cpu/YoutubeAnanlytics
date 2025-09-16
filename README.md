# YouTube Analytics Data Engineering Project

This project demonstrates an end-to-end data engineering pipeline using YouTube API v3, Azure Data Factory, Databricks, SQL Database, and Microsoft Fabric.
Data is ingested from YouTube API, processed with Medallion Architecture (Bronze → Silver → Gold) in Databricks, and finally visualized in Fabric Power BI reports.


![alt text](Project_Architecture-1.png)

🔹 Data Ingestion

# Collected data using YouTube Data API v3(Channel T-Series)

Stored raw JSON/CSV into Blob Storage (Bronze)

🔹 Data Transformation (Databricks)

Created Bronze → Silver → Gold layers

Cleaned and deduplicated data using PySpark

Applied transformations: filtering, aggregations, top 3 trending videos, etc.

🔹 Data Movement

Used ADF Copy Activity to move Gold tables → Azure SQL DB

🔹 Data Modeling

Built Fabric Semantic Model on top of SQL DB Gold tables

Performed final cleaning for reporting

🔹 Visualization

Created reports in Fabric Power BI (example: YouTube engagement distribution by published date, likes, comments, views, etc.)