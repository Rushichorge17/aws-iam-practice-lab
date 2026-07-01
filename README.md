# AWS IAM Practice Lab

## 📖 Project Overview

This project demonstrates the implementation of **AWS Identity and Access Management (IAM)** in a simulated enterprise environment.

The project covers creating IAM users, groups, roles, AWS managed policies, customer managed policies, password policies, and permission testing while following the **Principle of Least Privilege (PoLP)**.

---

# 🎯 Objectives

- Create IAM Users
- Create IAM Groups
- Configure Password Policy
- Create Customer Managed Policies
- Create IAM Roles
- Assign AWS Managed Policies
- Apply Principle of Least Privilege
- Perform Permission Testing

---

# 🏗️ Architecture

> **Note:** The architecture diagram is available in the `diagrams` folder.

![Architecture](diagrams/architecture.png)

---

# ☁️ AWS Services Used

- AWS IAM
- Amazon EC2
- Amazon S3

---

# 👥 IAM Users

| User | Group |
|------|-------|
| cloud-admin | Cloud Admins |
| developer1 | Developers |
| qa1 | QA |
| intern1 | Interns |
| audit1 | Auditors |
| finance1 | Finance |

---

# 👨‍💻 IAM Groups

- Cloud Admins
- Developers
- QA
- Interns
- Auditors
- HR
- Finance

---

# 🔐 Password Policy

Configured password policy:

- Minimum password length: **12 characters**
- At least one uppercase letter
- At least one lowercase letter
- At least one number
- At least one special character
- Password expires every **90 days**
- Prevent password reuse

---

# 📜 Customer Managed Policies

## EC2StartStopPolicy

Permissions:

- ec2:StartInstances
- ec2:StopInstances

---

## S3ReadOnlyPolicy

Permissions:

- s3:ListBucket
- s3:GetObject

---

## IAMAuditPolicy

Permissions:

- iam:ListUsers
- iam:GetUser
- iam:ListGroups

---

# 👤 IAM Role

## EC2-S3-Role

Attached Policy:

- AmazonS3ReadOnlyAccess

Purpose:

Allows Amazon EC2 instances to securely access Amazon S3 using temporary credentials.

---

# ✅ Permission Testing

| User | Expected Permissions |
|------|----------------------|
| cloud-admin | ✅ Create EC2<br>✅ Delete S3<br>✅ Create IAM Users |
| developer1 | ✅ Launch EC2<br>✅ Stop EC2<br>✅ View CloudWatch<br>❌ Cannot Create IAM Users |
| qa1 | ✅ View Resources<br>❌ Cannot Modify Resources |
| intern1 | ✅ View S3 Buckets<br>❌ Cannot Delete Objects<br>❌ Cannot Launch EC2 |
| audit1 | ✅ List IAM Users<br>❌ Cannot Create IAM Users |
| finance1 | ✅ View Billing<br>❌ Cannot Launch EC2 |

---

# 📂 Project Structure

```
aws-iam-practice-lab/
│
├── README.md
│
├── diagrams/
│   └── architecture.png
│
├── screenshots/
│   ├── iam-dashboard.png
│   ├── iam-users.png
│   ├── iam-groups.png
│   ├── password-policy.png
│   ├── managed-policies.png
│   ├── customer-managed-policies.png
│   ├── iam-role.png
│   └── permission-testing.png
│
└── policies/
    ├── EC2StartStopPolicy.json
    ├── S3ReadOnlyPolicy.json
    └── IAMAuditPolicy.json
```

---

# 📸 Screenshots

The screenshots below demonstrate each stage of the project.

- IAM Dashboard
- IAM Users
- IAM Groups
- Password Policy
- Customer Managed Policies
- IAM Role
- Permission Testing

> All screenshots are available in the `screenshots` folder.

---

# 📚 Skills Learned

- AWS IAM Fundamentals
- IAM Users
- IAM Groups
- IAM Roles
- AWS Managed Policies
- Customer Managed Policies
- IAM Policy JSON
- Principle of Least Privilege (PoLP)
- Role-Based Access Control (RBAC)
- Password Policies
- Permission Testing
- AWS Security Best Practices

---

# 🚀 Future Improvements

- Automate IAM user creation using AWS CLI
- Implement IAM using Terraform
- Configure Multi-Factor Authentication (MFA)
- Use IAM Identity Center
- Automate IAM deployment with Infrastructure as Code (IaC)

---

# 📖 References

- AWS IAM Documentation
- AWS Well-Architected Framework
- AWS Security Best Practices

---

# 👨‍💻 Author

**Rushikesh Chorge**

- GitHub: https://github.com/Rushichorge17

---
⭐ If you found this project useful, consider giving it a star!
