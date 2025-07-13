# Azure Data Factory Pipeline Project

This project includes ADF JSON pipeline templates and configurations for:

## 1. Self-hosted Integration Runtime (SHIR)
- Extracts data securely from on-premises servers.
- Loads data into Azure SQL Database.
- Requires SHIR to be installed and configured on a local server.

## 2. FTP/SFTP Data Extraction
- Connects to FTP/SFTP server to pull files.
- Uses linked service and dataset for flat file ingestion.

## 3. Incremental Load Pipeline
- Daily pipeline.
- Uses watermarking or change tracking to extract only new/modified rows.

## 4. Monthly Trigger
- Triggers the pipeline on the **last Saturday** of each month.
- Uses ADF expressions and custom recurrence settings.

## 5. Retry Logic for Data Retrieval
- Implements `retryPolicy` on activities.
- Waits and retries after transient failures like timeout or connectivity issues.

---

### Usage
1. Import these pipelines into Azure Data Factory via the Author UI or ARM template.
2. Modify linked services and datasets as per your environment.
3. Schedule triggers accordingly.
