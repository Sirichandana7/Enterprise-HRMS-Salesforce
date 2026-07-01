# Enterprise HRMS Object Dictionary

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

The Object Dictionary defines every Salesforce object used in the Enterprise HRMS application. It serves as a reference for administrators, developers, business analysts, QA engineers, and architects throughout the project lifecycle.

---

# Object Summary

| Object Label | API Name | Type | Record Name | Description |
|--------------|----------|------|-------------|-------------|
| Company | Company__c | Custom | Company Name | Stores company information |
| Location | Location__c | Custom | Location Name | Stores office locations |
| Department | Department__c | Custom | Department Name | Stores department details |
| Designation | Designation__c | Custom | Designation Name | Employee job roles |
| Employee | Employee__c | Custom | Employee Name | Master employee information |
| Emergency Contact | Emergency_Contact__c | Custom | Contact Name | Employee emergency contacts |
| Employee Document | Employee_Document__c | Custom | Document Name | Employee documents |
| Attendance | Attendance__c | Custom | Auto Number | Daily attendance |
| Leave Request | Leave_Request__c | Custom | Auto Number | Leave applications |
| Performance Review | Performance_Review__c | Custom | Auto Number | Performance evaluations |
| Training | Training__c | Custom | Training Name | Employee training |
| Asset | Asset__c | Custom | Asset Name | Assigned company assets |
| Candidate | Candidate__c | Custom | Candidate Name | Recruitment candidates |
| Interview | Interview__c | Custom | Auto Number | Interview schedule |
| Offer | Offer__c | Custom | Offer Number | Offer management |
| Onboarding | Onboarding__c | Custom | Auto Number | Employee onboarding |
| Background Verification | Background_Verification__c | Custom | Auto Number | Verification process |

---

# Object Details

## Employee

**Purpose**

Stores complete employee information.

**Owner**

HR Department

**Used By**

- HR
- Managers
- Payroll
- Agentforce

**Reports**

- Employee Master Report
- Employee Dashboard

**Automation**

- Welcome Email
- Employee ID Generation
- Onboarding Flow

---

## Department

Purpose

Stores all company departments.

Automation

- Department Head Assignment
- Department Reports

---

## Attendance

Purpose

Stores employee attendance.

Automation

- Daily Attendance Flow
- Working Hours Calculation

---

## Leave Request

Purpose

Stores leave requests.

Automation

- Approval Flow
- Leave Balance Update

---

## Performance Review

Purpose

Stores employee reviews.

Automation

- Review Reminder
- Goal Tracking

---

## Candidate

Purpose

Stores recruitment candidates.

Automation

- Interview Scheduling
- Resume Parsing (Future AI)

---

## Interview

Purpose

Interview scheduling.

Automation

- Interview Reminder
- Interview Feedback

---

## Offer

Purpose

Offer Letter Management.

Automation

- Offer Approval
- Email Offer Letter

---

## Onboarding

Purpose

Employee joining process.

Automation

- Welcome Kit
- IT Asset Allocation
- Training Assignment

---

# Future Objects

Future releases will include:

- Payroll
- Timesheet
- Expense
- Travel
- Rewards
- Recognition
- Internal Jobs
- Employee Wellness
- HR Case
- AI Feedback

---

# Conclusion

The Object Dictionary acts as the master reference for all Salesforce objects used in the Enterprise HRMS implementation.
