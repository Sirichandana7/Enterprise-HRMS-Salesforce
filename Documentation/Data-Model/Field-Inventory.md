# Enterprise HRMS Field Inventory

---

# Document Information

| Property | Value |
|----------|-------|
| Project | Enterprise HRMS |
| Platform | Salesforce |
| Prepared By | Mannava Siri Chandana |
| Version | 1.0 |
| Sprint | Sprint 5 |

---

# Introduction

The Field Inventory defines all fields required for the Enterprise HRMS application. It acts as the master reference for administrators and developers before creating custom fields in Salesforce.

---

# Employee Object

| Field Label | API Name | Data Type | Required | Description |
|--------------|----------|-----------|----------|-------------|
| Employee ID | Employee_ID__c | Auto Number | Yes | Unique employee identifier |
| Employee Name | Name | Text | Yes | Employee full name |
| Employee Code | Employee_Code__c | Text | Yes | Employee code |
| Official Email | Official_Email__c | Email | Yes | Company email |
| Personal Email | Personal_Email__c | Email | No | Personal email |
| Mobile Number | Mobile_Number__c | Phone | Yes | Contact number |
| Date of Birth | Date_of_Birth__c | Date | Yes | Employee DOB |
| Gender | Gender__c | Picklist | Yes | Gender |
| Joining Date | Joining_Date__c | Date | Yes | Joining date |
| Employment Type | Employment_Type__c | Picklist | Yes | Full Time, Contract, Intern |
| Employee Status | Employee_Status__c | Picklist | Yes | Active, Inactive, Resigned |
| Department | Department__c | Lookup | Yes | Department |
| Designation | Designation__c | Lookup | Yes | Designation |
| Location | Location__c | Lookup | Yes | Office Location |
| Reporting Manager | Reporting_Manager__c | Lookup(Employee) | No | Manager |
| Salary | Salary__c | Currency | No | Monthly salary |
| PAN Number | PAN_Number__c | Text | No | PAN |
| Aadhaar Number | Aadhaar_Number__c | Text | No | Aadhaar |
| Blood Group | Blood_Group__c | Picklist | No | Blood Group |
| Emergency Contact | Emergency_Contact__c | Lookup | No | Emergency Contact |

---

# Department Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Department Name | Name | Text |
| Department Code | Department_Code__c | Text |
| Department Head | Department_Head__c | Lookup(Employee) |
| Budget | Budget__c | Currency |
| Status | Status__c | Picklist |
| Description | Description__c | Long Text Area |

---

# Location Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Location Name | Name | Text |
| Country | Country__c | Picklist |
| State | State__c | Picklist |
| City | City__c | Text |
| Address | Address__c | Long Text Area |
| Postal Code | Postal_Code__c | Text |

---

# Designation Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Designation Name | Name | Text |
| Grade | Grade__c | Picklist |
| Job Level | Job_Level__c | Picklist |
| Minimum Salary | Minimum_Salary__c | Currency |
| Maximum Salary | Maximum_Salary__c | Currency |

---

# Attendance Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Attendance Date | Attendance_Date__c | Date |
| Employee | Employee__c | Master Detail |
| Check In | Check_In__c | Time |
| Check Out | Check_Out__c | Time |
| Working Hours | Working_Hours__c | Formula |
| Attendance Status | Attendance_Status__c | Picklist |

---

# Leave Request Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Employee | Employee__c | Master Detail |
| Leave Type | Leave_Type__c | Picklist |
| Start Date | Start_Date__c | Date |
| End Date | End_Date__c | Date |
| Total Days | Total_Days__c | Formula |
| Reason | Reason__c | Long Text Area |
| Status | Status__c | Picklist |

---

# Candidate Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Candidate Name | Name | Text |
| Email | Email__c | Email |
| Mobile | Mobile__c | Phone |
| Experience | Experience__c | Number |
| Applied Position | Applied_Position__c | Lookup |
| Resume | Resume__c | File |
| Status | Status__c | Picklist |

---

# Interview Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Candidate | Candidate__c | Master Detail |
| Interview Date | Interview_Date__c | Date |
| Interview Type | Interview_Type__c | Picklist |
| Interviewer | Interviewer__c | Lookup(User) |
| Result | Result__c | Picklist |

---

# Asset Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Asset Name | Name | Text |
| Asset Number | Asset_Number__c | Auto Number |
| Asset Type | Asset_Type__c | Picklist |
| Employee | Employee__c | Lookup |
| Status | Status__c | Picklist |

---

# Performance Review Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Employee | Employee__c | Master Detail |
| Review Date | Review_Date__c | Date |
| Rating | Rating__c | Picklist |
| Goal Achievement | Goal_Achievement__c | Percent |
| Manager Feedback | Manager_Feedback__c | Long Text Area |

---

# Training Object

| Field Label | API Name | Data Type |
|--------------|----------|-----------|
| Training Name | Name | Text |
| Trainer | Trainer__c | Lookup(User) |
| Training Date | Training_Date__c | Date |
| Completion Status | Completion_Status__c | Picklist |

---

# Agentforce Data Usage

| Object | Used by Agentforce |
|----------|--------------------|
| Employee | Yes |
| Attendance | Yes |
| Leave Request | Yes |
| Recruitment | Yes |
| Performance Review | Yes |
| Training | Yes |

---

# Conclusion

This Field Inventory serves as the blueprint for creating Salesforce fields, validation rules, page layouts, Flows, reports, dashboards, and Agentforce actions.
