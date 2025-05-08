# MS_Fabric_LAB_9
# Real-time Bicycle Observation Data Ingestion with Microsoft Fabric Eventstream

This project demonstrates how to use **Microsoft Fabric's Eventstream** feature to capture, transform, and route real-time events.

## Scenario
We simulate a real-time bike-share system, where event data streams report the number of bicycles available at collection points throughout a city.

## Steps Completed
- Created a **Fabric Workspace** with Fabric capacity.
- Created an **Eventhouse** and an associated **KQL Database**.
- Set up an **Eventstream** using sample bicycle data.
- Added a **Source** (`Bicycles`) to stream sample events.
- Added a **Destination** to load raw event data into a `bikes` table.
- Built a **Transformation**:
  - Aggregated the total number of bikes grouped by street every **5 seconds** using a **Tumbling Window**.
  - Loaded the transformed data into a `bikes-by-street` table.
- Queried real-time ingested and transformed data using **KQL (Kusto Query Language)**.

## Technologies Used
- Microsoft Fabric
- Eventstream
- Eventhouse
- KQL Database
- Kusto Query Language (KQL)

## Key Learnings
- Real-time event ingestion and processing using Microsoft Fabric.
- Data transformation with aggregation in streaming pipelines.
- Writing and modifying KQL queries to analyze real-time data.

## Notes
- Input data format: JSON
- Aggregation method: `SUM(No_Bikes)` grouped by `Street`
- Tumbling Window: 5 seconds
- Data can be visualized and monitored live in the Fabric workspace.

---
