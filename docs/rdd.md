# Requirements Definition Document (RDD) – LIFE TRACER
*Version 0.1.0 – Draft*

---

## 1. Introduction

### 1.1 Purpose of this Document
The purpose of this document is to define the user needs and goals for the LIFE TRACER project, providing a basis for subsequent system design and development.

### 1.2 Scope of the System
LIFE TRACER is a personal self-tracking tool to analyze time usage, support habit reflection, and generate periodic reports. The system will aggregate activity data collected from existing third-party services and provide visual summaries.

### 1.3 Definitions, Acronyms, and Abbreviations
| Term             | Definition                                                                 |
| ---------------- | -------------------------------------------------------------------------- |
| User             | Person using LIFE TRACER for self-tracking.                                |
| Activity Log     | Record of user actions, ideally in one-minute increments.                  |
| Aggregation      | Automatic summarization of activity data.                                  |
| Visualization    | Graphs, charts, dashboards for interpreting aggregated data.               |
| PDF Report       | Periodic export of summarized data in PDF format.                          |
| External Service | Third-party service integrated via APIs (e.g., Toggl, Notion, Coda).       |

### 1.4 References
- ISO/IEC/IEEE 29148:2018 Systems and software engineering — Life cycle processes — Requirements engineering
- Project personal notes on activity logging methodology

### 1.5 Overview of Document
This document contains user needs, system goals, use cases, assumptions, and constraints. It forms the basis for the subsequent System Requirements Specification (SRS).

---

## 2. Purpose and Background

### 2.1 Purpose
LIFE TRACER enables users to objectively reflect on their daily time usage, identify patterns, and support long-term self-improvement.

### 2.2 Background
The author has kept one-minute activity logs. Manual aggregation in Excel proved inefficient and limited insights. Automating collection and visualization will enable smoother reflection and analysis.

---

## 3. Goals and Objectives
The system shall:
1. Automate the collection of daily activity data.
2. Provide easy-to-understand visual summaries.
3. Enable periodic reporting in PDF format.
4. Support self-reflection and long-term habit improvement.

---

## 4. Stakeholders and Users

| Stakeholder Role | Description                                      |
| ---------------- | ------------------------------------------------ |
| Primary User     | Individual using the system for personal reflection and habit tracking. |
| Stakeholders     | None; project is self-contained.                |

---

## 5. System Scope

### 5.1 In-Scope
- Single-user personal use.
- Integration with existing third-party services (free-tier).
- Aggregation and visualization of activity data.
- PDF report generation.

### 5.2 Out-of-Scope
- Multi-user collaboration or sharing features.
- Development of a custom full-stack backend.
- Advanced UI/UX beyond dashboards provided by external services.

---

## 6. Use Cases / User Stories

| ID  | Use Case Description                                                            |
| --- | ------------------------------------------------------------------------------- |
| UC1 | User logs daily activities to review time usage.                                |
| UC2 | System automatically aggregates logged data to reduce manual work.              |
| UC3 | User views dashboards and visualizations to identify trends.                    |
| UC4 | User exports periodic PDF reports to maintain long-term records.                |

---

## 7. Assumptions and Constraints

### 7.1 Assumptions
- Users have personal accounts on external services.
- Data privacy is maintained through user-controlled accounts.
- The system relies on the free-tier of external services.

### 7.2 Constraints
- Single-user operation only.
- No multi-user functionality or collaboration.
- Security and data storage largely depend on the external service providers.

