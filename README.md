# Bright_Connect Call Centre Analytics (Tableau)

## Overview

This project simulates a real-world business intelligence consulting engagement for **BrightConnect**, a national utility services provider managing high-volume customer support operations across the United States.

The objective was to migrate existing Power BI dashboards to Tableau while standardizing KPI definitions, improving governance, and delivering a unified view of call centre performance.

---

## Problem Statement

Following a change in ownership, BrightConnect needed to align with a new enterprise analytics strategy centered on Tableau.

Key challenges included:

* Inconsistent KPI definitions across legacy dashboards
* Lack of unified visibility into call centre operations
* Need to preserve business insights during migration
* Limited ability to analyze SLA performance, agent productivity, and customer sentiment at scale 

---

## Objectives

* Rebuild call centre dashboards using Tableau
* Standardize SLA and performance metrics
* Enable interactive analysis across regions, channels, and agents
* Provide actionable insights for leadership and operations teams

---

## Business Impact

This solution enables:

* Real-time monitoring of SLA performance
* Identification of operational bottlenecks
* Improved agent performance tracking
* Better decision-making through unified reporting

---

## Tech Stack

* **Tableau** (Dashboard Development)
* **CSV Files** (Data Source)
* **Data Modeling** (Star Schema Design)

---


## Data Model

The solution is built using a **star schema**:

**Fact Table**

* Call Events

**Dimension Tables**

* Call Agents
* Call Centres

### Key Relationships

* `Call Events → Agent_ID → Call Agents`
* `Call Events → Call_Center_ID → Call Centres`

This structure enables flexible slicing across:

* Region
* Shift
* Channel
* Sentiment
* Capacity tier 

---

## Dashboard Overview

The Tableau dashboard provides a comprehensive operational view of call centre performance, including SLA tracking, agent productivity, and customer sentiment.

![Image](https://www.tableau.com/sites/default/files/2020-10/Screen%20Shot%202020-10-06%20at%203.31.21%20PM_0.png)

![Image](https://www.tableau.com/sites/default/files/call_center_2.png)

![Image](https://miro.medium.com/v2/resize%3Afit%3A1200/1%2AHR-zKvEjoLWTGKopcUh2DQ.png)

### Key Components

* KPI Summary (Total Calls, Avg Duration, CSAT)
* SLA Compliance Breakdown
* Calls by Day Heatmap
* Geographic Call Distribution
* Call Reason Analysis
* Channel Performance
* Agent Performance vs Targets
* Recent Call Activity Table

---

## KPIs Tracked

The dashboard answers key business questions such as:

* **Total Calls** → Volume of calls handled in a given period
* **SLA Compliance %** → Calls meeting SLA targets vs violations
* **Average Call Duration** → Efficiency of call handling
* **Customer Satisfaction (CSAT)** → Customer experience metric
* **Agent Performance vs Target** → Productivity benchmarking
* **Call Drivers** → Most common reasons for customer contact
* **Channel Effectiveness** → Efficiency by channel
* **Geographic Demand** → Call volume by state and city 

---

##  Key Insights

* Billing-related queries are the primary driver of call volume
* SLA compliance is a critical operational metric with noticeable violations
* Customer sentiment trends downward when SLA targets are missed
* Certain regions generate significantly higher call volumes
* Agent performance varies across experience levels and shifts

---


## How to Use

1. Download the Tableau workbook (`.twbx`) from the `/dashboards/tableau` folder
2. Open using Tableau Desktop
3. Use filters (Date, Sentiment, SLA Status) to explore insights
4. Interact with visuals to drill down into performance metrics

---


---

