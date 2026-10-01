# Auto Ticket Classification Using Flow Designer

## 📌 Project Overview

**Auto Ticket Classification using Flow Designer** is a ServiceNow-based automation project designed to simplify and automate the classification of IT support tickets in a school environment.

The school IT helpdesk receives multiple incident requests every day from students and teachers. These requests may include Wi-Fi connectivity problems, projector failures, password and login issues, and slow computer performance.

In a traditional helpdesk process, IT staff manually read each ticket, identify the issue, select the appropriate category and subcategory, and communicate the ticket status to the caller. This manual process can be time-consuming and may result in inconsistent classification.

This project automates the ticket classification process using **ServiceNow Flow Designer**. The flow analyzes keywords in the incident's **Short Description** and automatically assigns the appropriate **Category** and **Subcategory**.

The system also sends an automated email notification to the caller after the ticket is created.

The complete ServiceNow configuration is captured in a **Project Update Set**, which can be completed and exported as an XML file for transferring the configuration to another ServiceNow instance.

---

## 🎯 Project Objective

The main objective of this project is to reduce the manual effort involved in classifying IT support tickets.

The system is designed to:

- Automatically classify IT tickets based on the issue description.
- Analyze keywords in the Short Description.
- Automatically assign the appropriate Category.
- Automatically assign the appropriate Subcategory.
- Maintain a dependency between Category and Subcategory.
- Send an automated email notification to the caller.
- Store ticket information in a structured format.
- Reduce manual classification effort.
- Improve consistency in ticket categorization.
- Provide an easy-to-maintain and scalable no-code solution.

---

## ❗ Problem Statement

The school IT helpdesk receives multiple incident requests daily from students and teachers, such as:

- Wi-Fi issues
- Projector failures
- Password problems
- Login problems
- Slow computers
- System performance issues

Currently, IT staff manually review each request and assign a category and subcategory.

This process can be:

- Time-consuming
- Repetitive
- Error-prone
- Difficult to scale when ticket volume increases

Therefore, an automated ticket classification solution is required to reduce manual work and provide consistent ticket categorization.

---

## 💡 Proposed Solution

The proposed solution uses **ServiceNow Flow Designer** to automatically classify tickets.

When a new ticket is created:

1. The caller enters the required information.
2. The Short Description is provided.
3. The Flow Designer flow is triggered.
4. The flow checks the Short Description for predefined keywords.
5. An appropriate Category is identified.
6. The corresponding Subcategory is assigned.
7. The incident record is updated automatically.
8. An email confirmation is sent to the caller.

### Basic Workflow

```text
Student / Teacher
       |
       ↓
Create IT Ticket
       |
       ↓
Enter Caller + Short Description
       |
       ↓
Incident Workflow Record Created
       |
       ↓
ServiceNow Flow Designer
       |
       ↓
Check Short Description
       |
       ├───────────────┬────────────────┬────────────────┐
       ↓               ↓                ↓                ↓
      WiFi          Projector        Password          Slow
       ↓               ↓                ↓                ↓
   Network          Hardware          Access        Performance
       ↓               ↓                ↓                ↓
     Wi-Fi          Projector     Forgot Password   Slow Computer
       |
       ↓
Update Incident Record
       |
       ↓
Send Email to Caller
