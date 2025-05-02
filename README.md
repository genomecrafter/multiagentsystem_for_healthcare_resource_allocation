# Multi-Agent System for Healthcare Resource Allocation – Relevance AI

## Project Overview

This repository contains configuration files (`.rai`) for a **Multi-Agent System (MAS)** designed to assist in **real-time healthcare resource management** using **Relevance AI**. The agents work collaboratively to manage healthcare operations such as **demand forecasting**, **resource allocation**, and **procurement management**.

---

## Agent Architecture & Purpose

This MAS is composed of **three main agents**:

### 1. Demand Assessment Agent (DAA)
- Forecasts future healthcare demand using trends, historical data, and live inputs.
- Identifies potential shortages in resources like ICU beds, ventilators, oxygen, staff etc.
- Enhanced with a custom **Demand Forecasting Tool** to support proactive decisions.
- Other two agents RAA and PRMA are sub agents to DAA.

### 2. Resource Allocation Agent (RAA)
- Distributes and reallocates available medical resources dynamically.
- Considers criticality, equity, distance constraints, and urgency.
- Responds to alerts raised by DAA and ensures balanced distribution.

### 3. Procurement & Risk Management Agent (PRMA)
- Initiates external procurement when internal supplies are inadequate.
- Addresses transportation delays, low emergency drug stocks, and staff shortages.
- Capable of future integration with ticketing systems like ServiceNow for escalation.

All agents operate in coordination, sharing metadata and updates to simulate a real-time collaborative hospital support system.

---

## How to Use in Relevance AI

### Step 1: Import Agents
1. Log into [Relevance AI](https://www.relevanceai.com/).
2. Navigate to the **Agents** section.
3. Click on **Import Agent** and upload the provided `.rai` files for all the 3 agents.
4. Add RAA and PRMA as sub agents to DAA(Click on configure -> Naviagte to subagents subsection -> Click on add sub agent -> Select the sub agent).
5. Navigate to the **Tools** section.
6. Click on **Import Tool** and upload the provided file for Demand Forecasting tool in the repo.
7. Add this tool to DAA(Click on configure -> Naviagte to tools subsection -> Click on add tool -> Select the tool).

### Step 2: Set Up Triggers
- Use incoming email triggers (e.g., daily hospital status updates) to initiate agent workflows.
- Test agents with sample scenarios simulating emergency and normal situations.

### Step 3: Add Tools *(Optional for Paid Plans)*
- Integrate with ticketing tools like **ServiceNow** or **Remedy**.
- Enable email replies, API access, or dashboards on upgrade.

### Step 4: Simulate and Observe
- Monitor decisions made across different roles (DAA, RAA, PRMA) and you can suggest the agents to fine tune the response accordingly if you wish to do so.

---

## Resources

Access the detailed report, prototype working videos and some example test case scenarios in the following link :

🔗 [Google Drive – MAS Agent Resources](https://drive.google.com/drive/folders/1bONcdob9NL57Tbuuy_gB_qwEXeAvXZLs?usp=sharing)

---

## Notes & Limitations

- These agents are built using **Relevance AI’s free plan**, which includes:
  - 100 credits/day
  - 1 user
  - 10MB knowledge store
  - No API integrations
  - One-way trigger (no trigger reply support)
- Designed for **platform-agnostic deployment**; scalable in real-time with necessary extensions.
- Future plans include full deployment, round-trip email automation, and hospital API integration.
