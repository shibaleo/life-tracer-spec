# System Requirements Specification (SRS) – LIFE TRACER
*Version 0.1.0 – Draft*

---

## 1. Introduction

### 1.1 Purpose of this Document
This document specifies the system requirements for LIFE TRACER, providing a basis for system design, development, and validation. It details functional and non-functional requirements, external interfaces, and constraints.

### 1.2 Scope of the System
LIFE TRACER is a personal self-tracking tool that:
- Collects activity data from third-party services.
- Aggregates data in a backend (Supabase).
- Provides visual summaries via Grafana dashboards.
- Generates PDF reports from LaTeX templates.

### 1.3 References
- ISO/IEC/IEEE 29148:2018 Systems and software engineering — Life cycle processes — Requirements engineering
- Project notes on one-minute activity logging

### 1.4 Definitions, Acronyms, and Abbreviations
| Term             | Definition                                                                 |
| ---------------- | -------------------------------------------------------------------------- |
| User             | Person using LIFE TRACER for self-tracking.                                |
| Activity Log     | Record of user actions, ideally in one-minute increments.                  |
| Aggregation      | Automatic summarization of activity data.                                  |
| Visualization    | Graphs, charts, dashboards for interpreting aggregated data.               |
| PDF Report       | Periodic export of summarized data in PDF format.                          |
| External Service | Third-party service integrated via APIs (e.g., Toggl, Notion, Coda).       |

---

## 2. Functional Requirements

| Requirement ID | Description                                           | Priority    |
| -------------- | ----------------------------------------------------- | ----------- |
| FR-001         | Record daily activities in one-minute increments.    | High (MVP)  |
| FR-002         | Automatically aggregate logged data.                 | High        |
| FR-003         | Provide dashboards and visual summaries.             | High        |
| FR-004         | Generate and export PDF reports (LaTeX → Cloud).     | Medium      |

---

## 3. Non-functional Requirements

| Requirement ID | Description                                     | Priority |
| -------------- | ----------------------------------------------- | -------- |
| NFR-001        | Aggregation updates reflected within 30 seconds.| Medium   |
| NFR-002        | Visualizations responsive on desktop/mobile.    | Medium   |
| NFR-003        | All API communication must use HTTPS.           | High     |

---

## 4. External Interface Requirements

### 4.1 User Interfaces
- No custom UI development.
- Data entry via Toggl (time logs), Notion/Coda (memos), dashboards via Grafana.
- PDF report export via LaTeX templates compiled in cloud and uploaded to Google Cloud Storage.

### 4.2 APIs / External Services
- Toggl Track (time logging), Supabase (backend), Grafana Cloud (dashboards), Notion/Coda (notes).
- Authentication via OAuth2 or API keys.
- No public API provided by LIFE TRACER (initial release).

### 4.3 Data Interfaces
- Retrieve JSON data over HTTPS from external services.
- Internal data model examples:
  - **project_group**: project, group_color
  - **project**: name, color, active, status
  - **time_entry**: start, end, duration, project, tag, description, memo
  - **plan_entry**: start, end, duration, project, tag, description
- Aggregated results displayed in Grafana; data fed into LaTeX templates for PDF.

### 4.4 Hardware Interfaces
- PC, smartphone, wearable devices. No device-specific dependency.

---

## 5. Security Considerations (Q&A)

**Q1. How is user authentication handled?**
A1. Authentication relies on external services (OAuth2/API keys); no custom account system.

**Q2. Where is personal data stored?**
A2. In Supabase; data retrieved only from user’s own accounts.

**Q3. Is data encryption required?**
A3. HTTPS mandatory; at-rest encryption depends on Supabase.

**Q4. How is access control managed?**
A4. Single-user scope; multi-user features are out of scope.

**Q5. How are PDF reports protected?**
A5. Uploaded to Google Cloud Storage as private; sharing controlled by user.

**Q6. Are logs or audit trails maintained?**
A6. Not in initial release; optional simple logs may be stored.

**Q7. Security update policy?**
A7. Follow recommendations from external service providers.

---

## 6. Traceability Matrix (Draft)

| Requirement ID | Linked RDD Goal / Use Case          | Test Case (TBD) |
| -------------- | ---------------------------------- | --------------- |
| FR-001         | UC1: Log daily activities           | TBD             |
| FR-002         | UC2: Auto-aggregate data            | TBD             |
| FR-003         | UC3: View dashboards                | TBD             |
| FR-004         | UC4: Export PDF report              | TBD             |
| NFR-001        | Timely aggregation                  | TBD             |
| NFR-002        | Responsive dashboards               | TBD             |
| NFR-003        | Secure API communication            | TBD             |

---

## 7. Assumptions and Limitations
- No browser restrictions (web-based application).
- Single-user setup only; personal accounts.
- Security depends largely on external services.
- Initial release focuses on MVP functionality for individual use.

---

## 8. Appendix (Optional)
- Placeholder for sample data, API details, extended glossary, ER diagrams, future extension notes.
