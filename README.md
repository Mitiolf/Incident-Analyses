# Incident Analysis

## Project Overview

This project analyzes IT service management incident data to identify operational bottlenecks, SLA compliance issues, and patterns in incident resolution performance.

The goal of this analysis is to understand how incidents are distributed across teams, categories, and time, and to identify areas where the incident management process can be improved.

---

## Business Questions

The analysis focuses on answering the following questions:

**Operational:**

* Which teams are the slowest to resolve incidents?

* What types of incidents occur most often?

* Which categories generate the most SLA violations?

* Do weekend incidents have a longer resolution time?

**Process:**

* Where do bottlenecks occur?

* Do high priority actually shorten resolution time?

* How often are incidents reopened?

* Which teams have the highest reopen rate?

**Management:**

* What process improvements can shorten incident resolution time?

---

## Dataset

The dataset simulates IT Service Management (ITSM) incident records.

Main columns include:

| Column             | Description                                             |
| ------------------ | ------------------------------------------------------- |
| incident_id        | Unique identifier for the incident                      |
| created_date       | Time when the incident was reported                     |
| resolved_date      | Time when the incident was resolved                     |
| priority           | Incident priority level                                 |
| category           | Type of incident (Application, Database, Network, etc.) |
| assigned_team      | Team responsible for resolving the incident             |
| resolution_minutes | Time required to resolve the incident                   |
| sla_breached       | Indicates whether the SLA was exceeded                  |
| reopen_count       | Number of times the incident was reopened               |

---

## Tools Used

* Python
* Pandas
* Seaborn
* Matplotlib
* Jupyter Notebook

---

## Key Analyses Performed

### Data Cleaning

* Removal of invalid resolution times
* Identification of extreme outliers
* Conversion of date columns to datetime format

### Exploratory Data Analysis

* Incident distribution by category
* Incident distribution by team
* Resolution time analysis
* SLA breach analysis
* Priority vs resolution time analysis

### Process Analysis

* Incident routing between categories and teams
* Weekend vs weekday resolution performance
* Team workload vs resolution performance

---

## Key Insights

* Application incidents represent the largest share of total incidents.
* Weekend incidents tend to have longer resolution times.
* Some incident categories appear to be routed to non-specialized teams.

---

## Business Recommendations

1. Improve incident routing to ensure tickets are assigned to the correct specialist teams.
2. Improve knowledge base documentation to reduce incident reopen rates.
3. Introduce automated categorization to improve Service Desk efficiency.

---

## Project Structure

```
incident-analysis
│
├── data
│   incidents.csv
│
├── notebooks
│   EDA.ipynb
│
└── README.md
```

## Future Improvements

* Build an interactive dashboard (Power BI / Tableau)
* Add incident trend analysis over time
* Develop predictive models for SLA breach risk
