📦 Project Description: Direct Handling Scan Result Aggregation for ZLXH Site (Splunk Dashboard Input)
This SPL query powers part of a logistics operations dashboard by aggregating scan validation data from equipment and application logs at the ZLXH site. It focuses on Direct Handling (DH) operations, where packages (handling units) are scanned and assigned to loading units (LUs) as part of the sort and dispatch process.

The query performs the following:

Parses and enriches real-time scan validation logs using JSON field extraction.

Identifies Direct Handling areas via a lookup table to ensure only relevant operational zones are analyzed.

Extracts key scan metadata, such as barcodes, tracking numbers, sort plans, scan results, user/device IDs, and scan timestamps.

Appends historical LU creation events to enhance the context for each handling unit, ensuring the LU’s sort plan and rules are associated correctly even when not present in the scan logs.

Performs aggregation and filtering to provide a clear count of handling units scanned, categorized by sort plan, sort rule, and result status (e.g., success/failure).

Supports dashboard visualizations showing handling unit throughput and scan quality metrics for operational monitoring and quality assurance.

This query is designed to be efficient and modular, with dynamic field extraction and contextual enrichment to support real-time tracking and operational reporting in high-throughput logistics environments.

