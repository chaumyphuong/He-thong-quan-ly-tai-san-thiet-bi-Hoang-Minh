# User Interface & UX Design

This section describes the user interface structure, navigation flow, and key screens.  
The UI design focuses on usability, role-based access control, and operational efficiency.

---

## 1. System Navigation & User Flow

After logging in, each user is authenticated using a unique account.  
Upon successful login, the user is redirected to the **Home Dashboard**.

The system consists of **four main modules**, each with multiple sub-pages:

### 1.1 Asset Information Management
- Asset List
- Asset Detail View
- Add New Asset *(authorized users only)*
- Update Asset Information *(authorized users only)*

### 1.2 Asset Handover Management
- Handover Registration
- Handover Confirmation *(HR/Admin only)*
- Handover Records

### 1.3 Asset Return Management
- Return Registration
- Return Confirmation *(HR/Admin only)*
- Return Records

### 1.4 Reporting Module *(Authorized users only)*
- Assets by Project
- Assets by Condition
- Fully Depreciated Assets

---

## 2. Common System Features

### 2.1 Navigation Menu
- Provides access to all system modules:
  - Home
  - Asset Information
  - Asset Handover
  - Asset Return
  - Reports
- Supports collapse/expand for better workspace usage

### 2.2 Action Toolbar
Available on most screens:
- Refresh page
- Help & system guidance
- UI settings
- User profile
- Logout

### 2.3 Search Function
Supports searching by:
- Asset name
- Asset status
- Handover / Return record ID
- Project code

Search actions:
- Click search icon
- Press **ENTER**

### 2.4 Filtering & Pagination
- Result count display
- Pagination controls
- Date range filtering (DD/MM/YYYY)
- Attribute-based filters per screen

### 2.5 Sorting
- Ascending / descending
- Numeric → alphabetical priority

### 2.6 Auto Save (Draft Storage)
- Automatically saves form input
- Prevents data loss when leaving forms
- Applied to Add / Update / Registration forms

---

## 3. Login Screen

### Description
Allows users to authenticate and access the system.  
Credentials are validated against the **Account** database table.

### Components
- Username
- Password
- Remember Login option
- Login button

### Interaction
- `TAB` to navigate fields
- `ENTER` to submit
- Error message displayed for invalid credentials

---

## 4. Home Dashboard

### Description
Provides an overview of asset usage and system activity.

### Dashboard Widgets
- Asset usage status (in use vs available)
- Asset usage by department
- Asset usage by asset type
- Notifications panel (title & date)

---

## 5. Asset Information Management

### 5.1 Asset List
Displays all assets with:
- Asset ID (clickable)
- Asset name
- Asset type
- Purchase cost
- Purchase date
- Quantity
- Status
- Edit action

Features:
- Search & filter
- Add new asset
- Delete asset *(authorized users)*

---

### 5.2 Asset Detail View
Displays:
- Asset name & code
- Purchase date
- Depreciation period
- Cost & quantity
- Status
- Sub-assets (if any)
- Description
- Usage instructions

---

### 5.3 Add New Asset Form
*(Authorized users only)*

Fields include:
- Auto-filled entry date & user
- Asset code & name *(required)*
- Purchase cost (VND)
- Purchase date & depreciation period
- Quantity
- Asset condition
- Sub-asset relationship
- Description & usage guide

Actions:
- Reset
- Confirm

---

### 5.4 Update Asset Form
Allows:
- Editing asset information
- Deleting asset

Actions:
- Cancel
- Confirm update
- Delete asset

---

## 6. Asset Handover Management

### 6.1 Handover Registration
Includes:
- Entry date & user (auto-filled)
- Handover date & time
- Project code (DA-xxx)
- Asset selection & quantity

Actions:
- Cancel
- Submit request
- Print handover document

---

### 6.2 Handover Confirmation *(HR/Admin)*
Features:
- Search by record ID, project, asset
- Status filters
- Bulk confirmation
- Print handover record

---

### 6.3 Handover Records
Views differ by role:
- Employee
- HR/Admin

Includes:
- Record ID
- Project code
- Dates
- Asset list
- Status
- Actions (Print / Cancel / Confirm received)

---

## 7. Asset Return Management

### 7.1 Return Registration
Allows employees to:
- Select assets from previous handovers
- Specify return quantity
- Choose return date & time

---

### 7.2 Return Confirmation *(HR/Admin)*
Includes:
- Condition assessment
- Confirmation of receipt
- Status update

---

### 7.3 Return Records
Supports:
- Tracking return status
- Printing return documents
- Sorting & filtering

---

## 8. Reporting Module

### 8.1 Assets by Project
- Filter by project code & date range
- Export report as PDF
- Displays asset usage lifecycle

### 8.2 Assets by Condition
- Filter by asset condition
- Shows purchase & depreciation dates

### 8.3 Fully Depreciated Assets
- Lists assets reaching depreciation end
- Includes asset value & usage status

---

## 9. UI / UX Prototype

The system UI is visualized using a high-fidelity prototype.

🔗 **Figma Reference UI Kit:**  
https://www.figma.com/design/QyWA28PTmfFZBl2X2kShJo/Productivo-Dashboard-UI-Kit--Community-?node-id=403-17342&t=oYUiWUiJG2Iu4rzi-1

This prototype is used for:
- Requirement validation
- UI consistency reference
- Future frontend development
