# Data Flow Diagram (DFD)
## Asset & Equipment Management System

---

## 1. Context Diagram

### Overview
The Asset Management System (AMS) supports asset and equipment management, handover, return, and reporting activities within the organization.

### External Entities
- Administration & Human Resources Department
- Employees
- Management

### Interactions

#### Administration & Human Resources Department
- Create, update, and search asset/equipment information
- Confirm asset handover and return
- Update asset quantity and condition

#### Employees
- Search and view asset/equipment information
- Register handover and return requests
- Confirm receipt and return of assets

#### Management
- Request and view asset and equipment reports
- View reports by project, condition, and depreciation status

---

## 2. Level 0 Data Flow Diagram (DFD Level 0)

### Main Processes
1. Asset & Equipment Information Management  
2. Asset & Equipment Handover Management  
3. Asset & Equipment Return Management  
4. Asset & Equipment Reporting by Project  
5. Asset & Equipment Reporting by Status  
6. Reporting for Fully Depreciated Assets  
7. Asset & Equipment Search  

### Data Stores
- **D1: Asset & Equipment Data**
- **D2: Asset Handover & Return Data**

### Data Flow Summary
- Asset data is entered and maintained by Administration & HR.
- Employees submit handover and return requests.
- Management requests reports.
- The system retrieves and processes data from D1 and D2 to generate outputs.

---

## 3. Level 1 Data Flow Diagram (DFD Level 1)

---

### 3.1 Process 1.0 – Asset & Equipment Information Management

**Sub-processes**
- 1.1 View Asset & Equipment List  
- 1.2 Add New Asset  
- 1.3 Update Asset Information  
- 1.4 Delete Asset Information  

**Actors**
- Administration & Human Resources Department

---

### 3.2 Process 2.0 – Asset & Equipment Handover Management

**Sub-processes**
- 2.1 Register Handover Request  
- 2.2 View Handover Records  
- 2.3 Confirm Handover Request  
- 2.4 Execute Asset Handover  
- 2.5 Confirm Asset Receipt  

**Actors**
- Administration & Human Resources Department  
- Employees

---

### 3.3 Process 3.0 – Asset & Equipment Return Management

**Sub-processes**
- 3.1 Register Return Request  
- 3.2 View Return Records  
- 3.3 Confirm Return Request  
- 3.4 Recover Asset  
- 3.5 Confirm Asset Recovery  
- 3.6 Update Asset Status  

**Actors**
- Administration & Human Resources Department  
- Employees

---

### 3.4 Process 4.0 – Asset & Equipment Reporting by Project

**Sub-processes**
- 4.1 Submit Report Request  
- 4.2 Select Project  
- 4.3 Display Report  

**Actor**
- Management

---

### 3.5 Process 5.0 – Asset & Equipment Reporting by Status

**Sub-processes**
- 5.1 Submit Report Request  
- 5.2 Select Asset Status  
- 5.3 Display Report  

**Actor**
- Management

---

### 3.6 Process 6.0 – Reporting for Fully Depreciated Assets

**Sub-processes**
- 6.1 Submit Report Request  
- 6.2 Display Report  

**Actor**
- Management

---

### 3.7 Process 7.0 – Asset & Equipment Search

**Sub-processes**
- 7.1 Enter Search Keywords  
- 7.2 Apply Filters  
- 7.3 Display Search Results  

**Actors**
- Employees  
- Management

---

## 4. Level 2 Data Flow Diagram (DFD Level 2)

---

### 4.1 Decomposition of Process 1.1 – View Asset & Equipment List
- 1.1.1 View Asset Details  
  - Retrieve detailed asset information from **D1: Asset & Equipment Data**

---

### 4.2 Decomposition of Process 2.1 – Register Asset Handover

- 2.1.1 Enter Handover Information  
- 2.1.2 Select Asset & Equipment  
- 2.1.3 Submit Handover Request  

---

### 4.3 Decomposition of Process 2.3 – Confirm Handover Request

- 2.3.1 Cancel Handover Request  
- 2.3.2 Approve Handover and Prepare Assets  

---

### 4.4 Decomposition of Process 3.3 – Confirm Return Request

- 3.3.1 Cancel Return Request  
- 3.3.2 Approve Return and Prepare Asset Recovery  

---

## 5. Notes

This DFD documentation describes system boundaries, core processes, data flows, and process decomposition from Context Diagram to Level 2 DFD.

The diagrams support requirement validation and serve as a foundation for system design and future implementation.

---

## Keywords
Data Flow Diagram · System Analysis · Asset Management System · Business Analysis · DFD Level 0–2
