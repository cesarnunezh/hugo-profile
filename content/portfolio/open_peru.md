+++
title = 'Open Perú'
date = 2026-01-31T16:43:10-06:00
draft = true
+++
# **Civic Tech Platform for Legislative Transparency**

## Overview
**OpenPerú** is an open-source civic-tech platform that collects, processes, and structures public data from the Peruvian Congress to improve political transparency, accountability, and public access to legislative information. The project builds an end-to-end data pipeline that transforms fragmented and poorly structured government data into clean, queryable datasets and analytical tools.

![Open Peru](/assets/images/projects/openperu.png)

## Problem
Legislative information in Peru is:
- Highly fragmented across multiple web portals
- Published in inconsistent formats (HTML tables, PDFs, scanned documents)
- Difficult to track longitudinally (bills, committees, voting records, memberships)

This makes it hard for researchers, journalists, and citizens to analyze congressional behavior or hold representatives accountable.

## Solution
OpenPerú automates the full data lifecycle:
1. **Data extraction** from official congressional websites and APIs  
2. **Processing and normalization** into structured relational models  
3. **Versioning and change tracking** to monitor legislative updates over time  
4. **Foundations for analytics and visualization** to enable downstream research and civic use cases  

The system is designed to be extensible, reproducible, and transparent.

## Technical Architecture
- **Backend:** Python
- **Data Collection:** `httpx`, `Selenium`, `lxml`, `BeautifulSoup`  
- **OCR & Document Processing:** `Tesseract`, PDF text extraction pipelines
- **Data Modeling:** SQLAlchemy ORM, Pydantic schemas  
- **Databases:** SQLite
- **ETL Design:** Incremental updates, deduplication, change detection flags  
- **DevOps:** Docker, multi-stage builds, CI-friendly project structure  

## Key Features
- Scraping and tracking of:
  - Bills and legislative steps
  - Committees and memberships
  - Motions and voting outcomes
  - Congressional documents and revisions
- Robust enum mappings to standardize legislative states
- Explicit handling of temporal logic (legislative periods, memberships)
- Clear separation between **raw**, **processed**, and **analytics-ready** data layers

## Impact & Use Cases
- Enables empirical research on legislative behavior in Peru
- Lowers barriers for journalists and watchdog organizations
- Serves as a foundation for future tools such as:
  - Voting record dashboards
  - Bill progression tracking
  - Party cohesion and coalition analysis
  - Predictive models of legislative outcomes

## Status
🚧 **Active development**  
The platform is continuously expanding coverage and improving reliability, with plans for public APIs and visualization layers.

## Links
- GitHub Repository: [https://github.com/cesarnunezh/OpenPeru](https://github.com/cesarnunezh/OpenPeru)
- Documentation: *In progress*

---

*OpenPerú is part of a broader effort to use data engineering and open data to strengthen democratic and public policy accountability in Perú.*