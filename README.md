# Community-Solar-Credit-Allocation-Manager

## Problem Statement #63 — Sustainability & Green Tech

### Overview

The **Community Solar Credit Allocation Manager** is a clean-energy sharing portal designed to manage solar energy generation data, peer-to-peer solar credit transfers, and monthly utility billing offsets within a neighborhood microgrid.

The system receives rooftop solar generation metrics from smart meters and enables prosumer residents to transfer surplus solar credits to neighboring accounts.

### Target Stakeholders

- Prosumer Resident
- Co-op Manager

### Key Requirements

- Record solar generation data from smart meter feeds.
- Allow prosumers to transfer surplus solar credits to neighboring accounts.
- Track solar credit balances and monthly billing offsets.
- Process hourly generation data for multiple households.
- Maintain reliable and secure access to account and billing information.

### Lab 3 — Component Modelling & Architecture

For Lab 3, the system is modelled using a **Layered Architecture**.

The architecture is divided into:

1. **Presentation Layer**
   - Prosumer Portal / UI

2. **Business Layer**
   - Order Manager
   - Payment Service

3. **Data / Integration Layer**
   - Smart Meter Data Service
   - Solar Credit Database

### Component Interactions

The major interfaces between components include:

- **Credit Transfer API**
- **Payment Processing API**
- **Meter Telemetry API**
- **Credit / Account API**
- **Billing Data API**

These interfaces represent the flow of credit-transfer requests, payment/billing operations, smart-meter telemetry, and database interactions.

### Deliverables

This Lab 3 submission contains:

- UML Component Diagram
- Architectural Written Justification

### Repository Structure

```text
Lab3/
│
├── Lab3_Component_Diagram_Community_Solar.pdf
├── Lab3_Component_Diagram_Community_Solar.png
└── Lab3_Written_Justification_Community_Solar.pdf
