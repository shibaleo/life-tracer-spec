# Requirements Specification for LIFE TRACER

## 1. Cover & Basic Information
- Project Name: LIFE TRACER
- Version: 0.1.0
- Date: 2025-09-29
- Author: shibaleo
- Approver: TBD
- Purpose of Document: Specify the requirements for LIFE TRACER.
- Changelog: Initial draft

---

## 2. Purpose and Background

### Project Purpose
Provide a personal tool to analyze time usage and offer feedback for long-term growth.

### Background
Kept one-minute activity logs. Manual Excel aggregation was time-consuming and prevented insights. LIFE TRACER automates collection and visualization for easier reflection.

### Expected Use Cases
- Log daily activities; system aggregates automatically.
- View visual summaries to reflect on habits and support personal growth.

---

## 3. Scope

### In-scope (Initial Release)
- Collect personal data using existing services (free-tier).
- Store and aggregate data in a backend database.
- Visualize aggregated data, including PDF reports.

### Out-of-scope
- Full UI/UX design from scratch.
- Development of entirely new backend systems.
- Multi-user collaboration.

---

## 4. Glossary

| Term             | Definition                                                                 |
| ---------------- | -------------------------------------------------------------------------- |
| User             | Person using LIFE TRACER for self-tracking.                                |
| Activity Log     | Record of user actions, ideally in one-minute increments.                  |
| Aggregation      | Automatic summarization of activity data.                                  |
| Visualization    | Graphs, charts, dashboards for interpreting aggregated data.               |
| Backend          | Server/database storing collected data.                                    |
| External Service | Third-party service integrated via APIs.                                   |

---

## 5. Overall Description

### System Overview
Collects personal activity data from existing services, aggregates in backend, and provides visual summaries for reflection.

### Intended Users
Individual users seeking to analyze and improve time management.

### Constraints
- Uses free-tier external services; no full-stack development.
- Individual self-tracking only; no multi-user collaboration.
- Data privacy maintained via user-controlled accounts.
- Visualizations limited to integrated services or frontend dashboard capabilities.

---

## 6. Requirements List

### 6.1 Functional Requirements

| Requirement ID | Description                                          | Priority |
| -------------- | ---------------------------------------------------- | -------- |
| FR-001         | Log daily activities in one-minute increments.       | High     |
| FR-002         | Automatically aggregate logged data.                 | High     |
| FR-003         | View visual summaries of daily activities.           | High     |

### 6.2 Non-functional Requirements

| Requirement ID | Description                                     | Priority |
| -------------- | ----------------------------------------------- | -------- |
| NFR-001        | Aggregated data updated within 30 seconds.      | Medium   |
| NFR-002        | Visualizations responsive on desktop/mobile.    | Medium   |

### 6.3 Stakeholder Requirements

| Requirement ID | Description                                             | Priority |
| -------------- | ------------------------------------------------------- | -------- |
| SR-001         | Primarily use free services; avoid subscription costs.  | Medium   |

---

## 7. External Interface Requirements

### User Interfaces
- Input via third-party services (manual or wearable).
- View dashboards in real time; export PDFs.
- Accessible via PC or smartphone.

### APIs / External Services
- No public API provided.
- Integrate via available third-party APIs respecting auth and rate limits.

### Data Interfaces
- Retrieve data via JSON over HTTPS.
- Display aggregated results in dashboard; export as PDF.

### Hardware Interfaces
- PC, smartphone, or wearable devices. No device-specific dependency.

---

## 8. Traceability Matrix (Draft)

| Requirement ID | Description                                 | Source | Test Case ID | Test Case Description |
| -------------- | ------------------------------------------- | ------ | ------------ | --------------------- |
| FR-001         | Log daily activities                        | §6.1   | TBD          | TBD                   |
| FR-002         | Auto-aggregate logged data                  | §6.1   | TBD          | TBD                   |
| FR-003         | View visual summaries                       | §6.1   | TBD          | TBD                   |
| NFR-001        | Aggregation updated within 30s              | §6.2   | TBD          | TBD                   |
| NFR-002        | Responsive visualizations                   | §6.2   | TBD          | TBD                   |
| SR-001         | Use free services, avoid subscription costs | §6.3   | TBD          | TBD                   |

---

### Notes
- Test Case IDs and Descriptions are TBD; will be detailed in test specification phase.
- Ensures each requirement is traceable to at least one planned test case.

---
