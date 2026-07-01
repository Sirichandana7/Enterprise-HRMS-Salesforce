# Security Architecture

---

# Document Information

| Property | Value |
|----------|-------|
| Project | Enterprise Human Resource Management System (HRMS) |
| Client | ABC Global Technologies Pvt. Ltd. |
| Platform | Salesforce |
| Prepared By | Mannava Siri Chandana |
| Role | Salesforce Functional Consultant & Developer |
| Version | 1.0 |
| Sprint | Sprint 4 |

---

# 1. Introduction

The Security Architecture defines how users authenticate, access data, perform operations, and interact with the Enterprise HRMS application. The architecture follows Salesforce security best practices and the principle of least privilege to ensure that users can only access information required for their job responsibilities.

---

# 2. Security Objectives

The primary objectives are:

- Protect confidential employee information.
- Ensure role-based access control.
- Prevent unauthorized access.
- Secure sensitive HR records.
- Maintain audit trails.
- Support compliance requirements.
- Protect AI interactions through Agentforce.

---

# 3. Security Layers

```
                Users
                   │
        Authentication Layer
                   │
           Authorization Layer
                   │
            Record-Level Security
                   │
             Field-Level Security
                   │
             Object-Level Security
                   │
             Salesforce Database
```

---

# 4. User Roles

```
CEO
 │
HR Director
 │
HR Manager
 │
Recruitment Manager
 │
Recruiter
 │
Department Manager
 │
Employee
```

---

# 5. Profiles

The following Salesforce Profiles will be configured.

| Profile | Responsibilities |
|----------|------------------|
| System Administrator | Full System Access |
| HR Administrator | HR Operations |
| HR Executive | Employee Management |
| Recruiter | Recruitment Activities |
| Department Manager | Team Management |
| Employee | Self-Service |

---

# 6. Role Hierarchy

```
CEO

↓

HR Director

↓

HR Manager

↓

Department Manager

↓

Employee
```

The Role Hierarchy provides record visibility to managers while maintaining employee privacy.

---

# 7. Permission Sets

Separate Permission Sets will provide additional permissions without modifying Profiles.

Examples:

- Recruitment Operations
- Leave Management
- Attendance Management
- HR Analytics
- Report Access
- Agentforce Access
- Executive Dashboard Access

---

# 8. Organization-Wide Defaults (OWD)

| Object | OWD |
|----------|-----|
| Department | Public Read Only |
| Location | Public Read Only |
| Designation | Public Read Only |
| Employee | Private |
| Attendance | Private |
| Leave | Private |
| Performance | Private |
| Recruitment | Private |
| Documents | Private |

---

# 9. Sharing Rules

Sharing Rules will provide additional access where required.

Examples:

- HR Team can access all Employee records.
- Managers can access employees within their department.
- Recruiters can access Candidate records.
- Executives have read-only access to reports.

---

# 10. Field-Level Security

Sensitive fields include:

- Salary
- PAN Number
- Aadhaar Number
- Bank Account
- Medical Information
- Performance Rating

Only authorized Profiles and Permission Sets can view or edit these fields.

---

# 11. Login Security

Security settings include:

- Multi-Factor Authentication (MFA)
- Password Policies
- Login Hours
- Login IP Ranges
- Session Timeout
- Trusted IP Ranges

---

# 12. Data Protection

The application will implement:

- Encrypted Connections (HTTPS)
- Secure File Storage
- Field History Tracking
- Audit Trail
- Login History
- Data Backup Strategy

---

# 13. Agentforce Security

Agentforce will respect Salesforce security.

Features include:

- User Context Awareness
- Profile-Based Access
- Permission Set Validation
- Record-Level Security
- Field-Level Security
- Secure Prompt Execution

Example:

Employee asks:

"Show my salary."

↓

Agentforce

↓

Checks User Permissions

↓

If authorized → Displays salary.

If unauthorized → Returns Access Denied.

---

# 14. Security Monitoring

The following monitoring features will be enabled.

- Login History
- Setup Audit Trail
- Event Monitoring
- Field History Tracking
- Transaction Logs

---

# 15. Best Practices

- Principle of Least Privilege
- Avoid Hardcoded Credentials
- Use Permission Sets instead of multiple Profiles
- Enable MFA
- Use Sharing Rules instead of Public Access
- Protect Sensitive Data
- Review User Access Periodically

---

# 16. Advantages

- Enterprise-grade security
- Protection of confidential HR information
- Secure AI interactions
- Regulatory compliance
- Scalable access model
- Simplified administration

---

# 17. Future Enhancements

Future improvements may include:

- Salesforce Shield
- Platform Encryption
- Single Sign-On (SSO)
- Identity Provider Integration
- Conditional Access Policies
- Zero Trust Security

---

# 18. Conclusion

The Security Architecture ensures that the Enterprise HRMS application provides secure authentication, authorization, data protection, and controlled access while supporting Salesforce best practices and Agentforce AI capabilities.

The security model is designed to scale as the organization grows and to protect sensitive employee information throughout the employee lifecycle.
