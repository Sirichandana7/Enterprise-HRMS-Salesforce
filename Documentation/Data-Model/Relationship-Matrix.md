# Enterprise HRMS Relationship Matrix

---

## Project Information

| Property | Value |
|----------|-------|
| Project | Enterprise HRMS |
| Platform | Salesforce |
| Prepared By | Mannava Siri Chandana |
| Sprint | Sprint 5 |
| Version | 1.0 |

---

# Introduction

The Relationship Matrix defines how Salesforce objects are connected within the Enterprise HRMS application. Selecting the appropriate relationship type ensures data integrity, scalability, reporting capabilities, and security.

---

# Relationship Matrix

| Parent Object | Child Object | Relationship | Cardinality | Reason |
|---------------|--------------|--------------|-------------|--------|
| Company | Location | Lookup | 1:M | Multiple office locations |
| Location | Department | Lookup | 1:M | Departments belong to a location |
| Department | Employee | Lookup | 1:M | Employees work in departments |
| Designation | Employee | Lookup | 1:M | Job titles reused across employees |
| Employee | Emergency Contact | Master-Detail | 1:M | Dependent on employee |
| Employee | Employee Document | Master-Detail | 1:M | Employee-owned documents |
| Employee | Attendance | Master-Detail | 1:M | Attendance belongs to employee |
| Employee | Leave Request | Master-Detail | 1:M | Leave records belong to employee |
| Employee | Performance Review | Master-Detail | 1:M | Performance linked to employee |
| Employee | Training | Lookup | 1:M | Training history retained |
| Employee | Asset | Lookup | 1:M | Assets may be reassigned |
| Candidate | Interview | Master-Detail | 1:M | Interview depends on candidate |
| Candidate | Offer | Lookup | 1:M | Offer retained independently |
| Offer | Onboarding | Lookup | 1:1 | Onboarding begins after offer |
| Employee | Exit Process | Lookup | 1:1 | Exit process after resignation |

---

# Relationship Diagram

```text
Company
   │
Location
   │
Department
   │
Designation
   │
Employee
   ├── Emergency Contact
   ├── Employee Document
   ├── Attendance
   ├── Leave Request
   ├── Performance Review
   ├── Training
   ├── Asset
   └── Exit Process

Candidate
   │
Interview
   │
Offer
   │
Onboarding
```

---

# Lookup Relationships

Used when:

- Child records should exist independently.
- Parent deletion should not delete child records.
- Flexible ownership is required.

Examples:

- Department → Employee
- Employee → Asset
- Employee → Training

---

# Master-Detail Relationships

Used when:

- Child records depend completely on the parent.
- Parent deletion should delete child records.
- Roll-Up Summary fields are required.

Examples:

- Employee → Attendance
- Employee → Leave Request
- Employee → Employee Document
- Candidate → Interview

---

# Design Decisions

Why Lookup?

- Assets can be reassigned.
- Departments exist independently.
- Locations remain even if departments change.

Why Master-Detail?

- Attendance cannot exist without an employee.
- Leave records depend on employees.
- Interviews belong to candidates.

---

# Future Relationships

Future modules will include:

- Employee → Expense
- Employee → Travel Request
- Employee → Recognition
- Employee → Rewards
- Employee → Skills
- Employee → Certification
- Employee → Timesheet

---

# Conclusion

This Relationship Matrix provides the foundation for creating Salesforce objects, configuring automation, building reports, implementing security, and enabling Agentforce.
