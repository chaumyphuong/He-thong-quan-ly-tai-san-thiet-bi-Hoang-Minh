## 1. Entity Relationship Diagram (ERD)

The system consists of **7 main entities**:

- Asset
- Employee
- Department
- Project
- Account
- Asset Handover Record
- Asset Return Record

### Entity Relationships

- **Asset – Sub Asset (Component)**
  - An asset can consist of multiple sub-assets (components).
  - Sub-assets are also considered assets and have their own asset codes.
  - This is a **many-to-many (N–N)** self-referencing relationship.

- **Employee – Department**
  - One department can have many employees.
  - Each employee belongs to one department.
  - Relationship type: **1–N**

- **Employee – Project**
  - An employee can participate in multiple projects.
  - A project can have multiple employees.
  - Relationship type: **N–N**
  - The relationship includes an additional attribute: **role** of the employee in the project.

- **Employee – Account**
  - Each employee has exactly one system account.
  - Relationship type: **1–1**

- **Employee – Asset**
  - Assets are handed over to employees and returned after project completion.
  - This relationship is implemented through:
    - Asset Handover Record
    - Asset Return Record
## 2. Database Schema Overview

The database consists of the following tables:

1. asset
2. asset_component
3. employee
4. account
5. department
6. project
7. project_participation
8. asset_handover
9. asset_return

### Data Sources
- Asset data is retrieved from:
  - `asset`
  - `asset_component`
- Asset handover and return data is retrieved from:
  - `asset_handover`
  - `asset_return`

## 3. Data Table:
### 3.1. Asset Table (tai_san):
## 3. Database Tables

### 3.1. Asset Table (tai_san)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                  |
|--------------------|-------------|--------|---------------|------------------------------|
| maTB               | char        | 4      | Not null      | Asset ID (Primary Key)       |
| tenTB              | nvarchar    | 35     | Not null      | Asset Name                   |
| tgmua              | date        |        | Not null      | Purchase Date                |
| tgkhauhao          | date        |        | Not null      | Depreciation Date            |
| loai               | nvarchar    | 25     | Null          | Asset Type                   |
| Tinhtrang          | nvarchar    | 70     | Not null      | Asset Status                 |
| chiphi             | money       |        | Not null      | Purchase Cost                |
| mota               | nvarchar    | 200    | Null          | Asset Description            |
| HDSD               | nvarchar    | 300    | Null          | Usage Guide                  |
| maNV               | char        | 4      | Not null      | Employee ID (Foreign Key)    |

### 3.2. Project Table (du_an)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                  |
|--------------------|-------------|--------|---------------|------------------------------|
| maDA               | char        | 4      | Not null      | Project ID (Primary Key)     |
| tenDA              | nvarchar    | 40     | Not null      | Project Name                 |
| mota               | nvarchar    | 200    | Null          | Project Description          |
| khachhang          | nvarchar    | 40     | Null          | Client                       |
| ngaybatdau         | date        |        | Not null      | Start Date                   |
| ngayketthuc        | date        |        | Not null      | End Date                     |

### 3.3. Department Table (phong_ban)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                  |
|--------------------|-------------|--------|---------------|------------------------------|
| maPB               | char        | 4      | Not null      | Department ID (Primary Key)  |
| tenphong           | nvarchar    | 30     | Not null      | Department Name              |

### 3.4. Employee Table (nhan_vien)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                     |
|--------------------|-------------|--------|---------------|---------------------------------|
| maNV               | char        | 4      | Not null      | Employee ID (Primary Key)       |
| ho                 | nvarchar    | 15     | Not null      | Last Name                       |
| tendem             | nvarchar    | 30     | Null          | Middle Name                     |
| ten                | nvarchar    | 15     | Not null      | First Name                      |
| diachi             | nvarchar    | 100    | Not null      | Address                         |
| chucvu             | nvarchar    | 25     | Not null      | Position                        |
| SDT                | varchar     | 12     | Not null      | Phone Number                    |
| gioitinh           | char        | 1      | Not null      | Gender                          |
| ngaysinh           | date        |        | Null          | Date of Birth                   |
| luong              | money       |        | Not null      | Salary                          |
| maphong            | char        | 4      | Not null      | Department ID (Foreign Key)     |

### 3.5. Account Table (tai_khoan)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                  |
|--------------------|-------------|--------|---------------|------------------------------|
| tenTK              | varchar     | 20     | Not null      | Username                     |
| matkhau            | varchar     | 20     | Not null      | Password                     |
| maNV               | char        | 4      | Not null      | Employee ID (Foreign Key)    |

### 3.6. Handover Record Table (bienban_giao)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                        |
|--------------------|-------------|--------|---------------|------------------------------------|
| maNV               | char        | 4      | Not null      | Receiving Employee ID              |
| tggiao             | date        |        | Not null      | Handover Date                      |
| maNVgiao           | char        | 4      | Not null      | Handing-over Employee ID (FK)      |
| maTB               | char        | 4      | Not null      | Asset ID (Foreign Key)             |

### 3.7. Return Record Table (bienban_tra)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                        |
|--------------------|-------------|--------|---------------|------------------------------------|
| maNV               | char        | 4      | Not null      | Returning Employee ID              |
| tgtra              | date        |        | Not null      | Return Date                        |
| maNVnhan           | char        | 4      | Not null      | Receiving Employee ID (FK)         |
| tinhtrangtra       | nvarchar    | 25     | Not null      | Return Status                      |
| maTB               | char        | 4      | Not null      | Asset ID (Foreign Key)             |

### 3.8. Project Participation Table (tham_gia)

| Attribute Name     | Data Type   | Length | Null/Not Null | Description                        |
|--------------------|-------------|--------|---------------|------------------------------------|
| maDA               | char        | 4      | Not null      | Project ID (Composite Primary Key) |
| maNV               | char        | 4      | Not null      | Employee ID (Composite Primary Key)|
| vaitro             | nvarchar    | 25     | Null          | Role in Project                    |
