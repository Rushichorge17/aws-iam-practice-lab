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

                                AWS Cloud
┌──────────────────────────────────────────────────────────────────────────────┐
│                              AWS Account                                     │
│                                                                              │
│  ┌──────────────────────────── IAM ───────────────────────────────────────┐  │
│  │                                                                       │  │
│  │  IAM Groups                                                           │  │
│  │                                                                       │  │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐  ┌─────────────┐ │  │
│  │  │ Cloud Admins │  │ Developers   │  │ QA Team      │  │ Auditors    │ │  │
│  │  └──────┬───────┘  └──────┬───────┘  └──────┬───────┘  └──────┬──────┘ │  │
│  │         │                 │                 │                 │         │  │
│  │         │                 │                 │                 │         │  │
│  │ cloud-admin         developer1        qa1           audit1              │  │
│  │ finance1            intern1                                           │  │
│  │                                                                       │  │
│  └───────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
│                 Customer Managed Policies                                    │
│                                                                              │
│     ┌──────────────────┐    ┌─────────────────┐    ┌──────────────────┐      │
│     │ EC2StartStop     │    │ S3ReadOnly      │    │ IAMAudit         │      │
│     └────────┬─────────┘    └────────┬────────┘    └────────┬─────────┘      │
│              │                       │                      │                │
│              └──────────────┬────────┴──────────────┐       │                │
│                             │                       │       │                │
│                         IAM Groups receive Policies         │                │
│                                                             │                │
│                                                                              │
│                         IAM Role                                              │
│                    ┌────────────────┐                                         │
│                    │ EC2-S3-Role    │                                         │
│                    └───────┬────────┘                                         │
│                            │                                                  │
│                            ▼                                                  │
│                     Amazon EC2 Instance                                       │
│                            │                                                  │
│                            ▼                                                  │
│                     Amazon S3 Bucket                                          │
│                                                                              │
└──────────────────────────────────────────────────────────────────────────────┘

## Author

Rushikesh Chorge
