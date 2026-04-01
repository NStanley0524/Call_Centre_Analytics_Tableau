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

![Image](https://public.tableau.com/views/CallCentreAnalysis_17678002096380/Dashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


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

## Insights & Recommendations

### 1. SLA Performance is a Critical Risk
**Insight**  
- 31.77% of calls violate SLA  
- Only 68.23% are handled within SLA  
- Nearly 1 in 3 customers experience delays  

**Impact**  
- Increased customer dissatisfaction  
- Higher repeat call volume  
- Rising operational costs  

**Recommendations**  
- Analyze SLA breaches by call reason, agent, and time of day  
- Introduce priority routing for high-impact calls (e.g. outages)  
- Set real-time alerts when SLA violations exceed threshold levels  

---

### 2. Billing Issues Drive Call Volume
**Insight**  
- Billing-related queries are the highest driver of calls (~40%+)  
- Significantly higher than other categories  

**Impact**  
- Indicates upstream issues (unclear billing, poor self-service)  
- Adds unnecessary load on call centre operations  

**Recommendations**  
- Improve billing clarity (statements, FAQs, UI/UX)  
- Introduce chatbot flows specifically for billing queries  
- Create a dedicated billing support queue with specialized agents  

---

### 3. Customer Sentiment is Skewed Negative
**Insight**  
- Neutral and negative sentiments dominate  
- Positive experiences are significantly lower  

**Impact**  
- Indicates inconsistent service quality  
- Likely linked to SLA delays and long call durations  

**Recommendations**  
- Correlate sentiment with SLA and call duration  
- Train agents on handling high-friction scenarios (billing, outages)  
- Implement post-call recovery strategies for negative experiences  

---

### 4. High Average Call Duration Reduces Efficiency
**Insight**  
- Average call duration is ~12.33 minutes  

**Impact**  
- Fewer calls handled per agent  
- Contributes directly to SLA violations  

**Recommendations**  
- Break down call duration by call reason  
- Develop standardized resolution scripts  
- Route calls to specialized agents to reduce handling time  

---

### 5. Variability in Agent Performance
**Insight**  
- Some agents consistently meet targets while others fall short  

**Impact**  
- Inconsistent service delivery  
- Missed productivity opportunities  

**Recommendations**  
- Identify top-performing agents and replicate best practices  
- Provide targeted coaching for underperforming agents  
- Align high-performing agents with peak demand periods  

---

### 6. Uneven Call Distribution Across Days
**Insight**  
- Call volume shows clear peaks on specific days  

**Impact**  
- Staffing may not align with demand patterns  
- Leads to avoidable SLA breaches  

**Recommendations**  
- Optimize staffing based on demand patterns  
- Introduce flexible or overflow staffing models  
- Use historical data to forecast call volumes  

---

### 7. Geographic Concentration of Demand
**Insight**  
- Certain states contribute disproportionately to call volume  

**Impact**  
- Regional issues may be driving demand  
- Uneven operational load across locations  

**Recommendations**  
- Conduct region-specific root cause analysis  
- Deploy localized support strategies  
- Launch targeted communication to reduce avoidable calls  

---

### 8. Underutilization of Digital Channels
**Insight**  
- Majority of interactions occur via call center  
- Chatbot and web channels are underused  

**Impact**  
- Higher operational costs  
- Missed opportunity for automation  

**Recommendations**  
- Enhance chatbot capabilities for common issues  
- Improve self-service experience on web platforms  
- Incentivize customers to use digital channels  

---

## Strategic Summary

The analysis highlights that the call centre is currently operating in a **reactive mode**, driven by high call volumes, SLA inefficiencies, and limited use of automation.

### Key Focus Areas:
- Reduce call volume through better self-service (especially billing)  
- Improve SLA performance through smarter routing and staffing  
- Enhance agent productivity and consistency  
- Shift demand toward digital channels  

Addressing these areas will lead to improved customer satisfaction, lower operational costs, and more scalable operations.

---


## How to Use

1. Download the Tableau workbook (`.twbx`) from the `/dashboards/tableau` folder
2. Open using Tableau Desktop
3. Use filters (Date, Sentiment, SLA Status) to explore insights
4. Interact with visuals to drill down into performance metrics

---


---

