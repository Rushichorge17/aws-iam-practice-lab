# AWS IAM Practice Lab

## Project Overview

This project demonstrates Identity and Access Management (IAM) in AWS.

## AWS Services Used

- IAM Users
- IAM Groups
- IAM Roles
- AWS Managed Policies
- Customer Managed Policies

## Groups

- Admins
- Developers
- QA
- Interns
- Auditors
- HR
- Finance

## Custom Policies

- IAMAuditPolicy
- S3ReadOnlyPolicy
- EC2StartStopPolicy

## Skills Learned

- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- Principle of Least Privilege
- AWS Managed Policies
- Customer Managed Policies

## Screenshots

See the `screenshots` folder.

##Architecture
                         AWS Account
                              │
 ┌────────────────────────────┴────────────────────────────┐
 │                                                         │
 │                     IAM                                 │
 │                                                         │
 │  ┌─────────────┐   ┌──────────────┐   ┌──────────────┐  │
 │  │Cloud Admins │   │ Developers   │   │ QA Team      │  │
 │  └──────┬──────┘   └──────┬───────┘   └──────┬───────┘  │
 │         │                 │                  │          │
 │  cloud-admin        developer1             qa1          │
 │                                                         │
 │  ┌─────────────┐   ┌──────────────┐   ┌──────────────┐  │
 │  │ Interns     │   │ Auditors     │   │ Finance      │  │
 │  └──────┬──────┘   └──────┬───────┘   └──────┬───────┘  │
 │         │                 │                  │          │
 │    intern1            audit1           finance1         │
 │                                                         │
 └─────────────────────────────────────────────────────────┘
                              │
                Customer Managed Policies
                              │
      ┌──────────────┬───────────────┬──────────────┐
      │              │               │              │
 EC2 Start/Stop   S3 Read Only   IAM Audit   Billing ReadOnly
                              │
                         IAM Role
                       EC2-S3-Role
                              │
                        Amazon EC2
                              │
                        Amazon S3

## Author

Rushikesh Chorge
