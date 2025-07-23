---
📁 Title: IT Equipment Request & Fulfillment Portal
📌 Type: Scoped Application (Studio)
🗃 Upload Target: GitHub repository (.xml or Update Set)
---

# IT Equipment Request & Fulfillment Portal

A ServiceNow custom scoped application that allows employees to request IT equipment and tracks the entire lifecycle from request to fulfillment. This application demonstrates how to implement core ServiceNow features such as SLAs, automated email notifications, dashboards, knowledge articles, and reporting — all within a clean, modular design.

---

## 🚀 Project Features

- Custom data model with Equipment Request, Catalog, and Fulfillment records
- SLA definitions based on request priority
- Email notifications for lifecycle events (submission, assignment, fulfillment, SLA breach)
- Performance analytics with visual dashboards and reports
- Knowledge Base integration with helpful articles for users
- Approval and assignment workflows using Workflow Studio
- Scoped application with Git integration

---

## 🧱 Data Model

- Table: x_yourapp_equipment_request
- Table: x_1778869_it_eq_equipment_request extends task

  - Fields: requested_for (reference sys_user), fulfillment_manager (reference sys_user), equipment_type (reference x_1778869_it_eq_equipment_catalog), justification, status, priority, assigned_to (reference sys_user), delivery_date, fulfillment_notes, fulfillment_status, department (reference cmn_department)

- Table: x_1778869_it_eq_equipment_catalog

  - Fields: is_available, number, description, cost_estimate, model_number, name, image

---

## 🔔 Notifications

| Trigger           | Recipient          | Description                    |
| ----------------- | ------------------ | ------------------------------ |
| Request Submitted | Requester          | Confirmation email             |
| Request Assigned  | Assigned Fulfiller | Email with task details        |
| SLA Breached      | Manager/Approver   | Escalation email               |
| Request Fulfilled | Requester          | Completion and feedback survey |

---

## 📊 Reports & Dashboards

- Pie Chart: Requests by Priority
- Bar Graph: SLA Compliance per Month
- List: Requests Pending Approval
- Scorecard: Average Fulfillment Time

These reports are displayed on a centralized dashboard for IT managers.

---

## 📚 Knowledge Articles

Published articles include:

- “How to Submit an Equipment Request”
- “Expected Delivery Times by Equipment Type”
- “Troubleshooting Your Laptop or Monitor”
- “Contact IT Support”

Each article is linked contextually on the request form and within the portal.

---

## 🔁 Workflow

1. Employee submits equipment request
2. Optional approval based on cost/department
3. Task is assigned to IT staff
4. SLA timers start based on priority
5. Fulfiller updates task upon delivery
6. Notifications sent at each stage
7. Data collected for dashboard/reporting

---

## 🎓 Learning Outcomes

✅ Creating scoped apps in Studio

✅ Design and implement custom tables and relationships

✅ Use Workflow Studio for notification and approval logic

✅ Configure SLA definitions with pause/resume/stop conditions

✅ Publish and link Knowledge Articles to enhance self-service

✅ Build reports, visual dashboards, and performance analytics

✅ Use update sets and GitHub to version and share applications

✅ Follow a structured SDLC approach with documentation

---

## 🛠 Setup Instructions

1. Clone/download the repo into your local dev environment
2. Import the Update Set or App XML into your ServiceNow PDI
3. Navigate to the “IT Equipment Portal” module
4. Test by submitting a new request
5. Explore the reports, SLAs, workflows, and knowledge articles

---

## 📂 Repository Structure

- /update_sets/
- /screenshots/
- /documentation/
- README.md
