**What is an ER Diagram?**


An Entity Relationship Diagram (ERD) shows:

**What objects exist**
**How they're connected**
Cardinality (One-to-One, One-to-Many)
Parent-child relationships

In Salesforce, this helps us decide between:

Lookup Relationships
Master-Detail Relationships

**HRMS Enterprise Data Model**

Company
│
├── Location
│      │
│      ├── Department
│      │       │
│      │       ├── Designation
│      │       │       │
│      │       │       ├── Employee
│      │       │       │      │
│      │       │       │      ├── Emergency Contact
│      │       │       │      ├── Employee Document
│      │       │       │      ├── Attendance
│      │       │       │      ├── Leave Request
│      │       │       │      ├── Performance Review
│      │       │       │      ├── Training
│      │       │       │      ├── Asset
│      │       │       │      ├── Payroll (Simulation)
│      │       │       │      ├── Exit Process
│      │       │       │      └── ID Card
│      │       │
│      │       └── Recruitment
│      │              │
│      │              ├── Candidate
│      │              ├── Interview
│      │              ├── Offer
│      │              ├── Onboarding
│      │              └── Background Verification


**Core Objects**

| Object             | Purpose                |
| ------------------ | ---------------------- |
| Location           | Company offices        |
| Department         | Business units         |
| Designation        | Job titles             |
| Employee           | Employee master data   |
| Emergency Contact  | Family details         |
| Employee Document  | Certificates, IDs      |
| Attendance         | Daily attendance       |
| Leave Request      | Employee leave         |
| Performance Review | Performance management |
| Training           | Learning records       |
| Asset              | Laptop, ID card, etc.  |
| Candidate          | Recruitment            |
| Interview          | Interview process      |
| Offer              | Offer letters          |
| Onboarding         | Joining process        |

**Relationship Overview**


| Parent      | Child              | Relationship  |
| ----------- | ------------------ | ------------- |
| Location    | Department         | Lookup        |
| Department  | Employee           | Lookup        |
| Designation | Employee           | Lookup        |
| Employee    | Attendance         | Master-Detail |
| Employee    | Leave Request      | Master-Detail |
| Employee    | Performance Review | Master-Detail |
| Employee    | Employee Document  | Master-Detail |
| Candidate   | Interview          | Master-Detail |
| Candidate   | Offer              | Lookup        |
| Offer       | Onboarding         | Lookup        |

