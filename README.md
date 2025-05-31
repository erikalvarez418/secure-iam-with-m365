# Microsoft 365 Zero Trust Lab

## Overview

This lab demonstrates how to secure a Microsoft 365 tenant using Entra ID (formerly Azure Active Directory), Microsoft Intune, and Conditional Access policies. The focus is on implementing Zero Trust principles by enforcing strong identity management, device compliance, and adaptive access controls.

This project simulates a real-world MSP or enterprise scenario and can be used to showcase hands-on security experience.

## Objectives

- Enable Multi-Factor Authentication (MFA) for users
- Block legacy authentication protocols
- Enforce risk-based Conditional Access policies
- Restrict access from non-compliant or unmanaged devices
- Align Microsoft 365 administration with cybersecurity best practices

## Lab Environment

| Component         | Details                              |
|------------------|--------------------------------------|
| Tenant           | Microsoft 365 Developer E5           |
| Directory        | Microsoft Entra ID (Azure AD)        |
| Device Management| Microsoft Intune                     |
| Users            | 1–2 test users for simulation        |
| Admin Tools      | Entra Admin Center, Intune Portal    |

## Zero Trust Components Implemented

| Component                  | Tool Used                    | Outcome                                                |
|----------------------------|------------------------------|---------------------------------------------------------|
| Multi-Factor Authentication| Entra ID                     | Prevents unauthorized access through MFA enforcement    |
| Block Legacy Authentication| Conditional Access           | Disallows protocols that bypass modern security controls|
| Risk-Based Access          | Entra ID Identity Protection | Triggers MFA for risky sign-ins                        |
| Device Compliance          | Intune + Conditional Access  | Blocks access from unmanaged or non-compliant devices   |

## Project Structure

- `mfa-setup.md` — Guide and screenshots for enabling MFA
- `block-legacy-auth.md` — Policy steps to block legacy authentication
- `risk-based-mfa.md` — Guide for MFA on risky sign-ins
- `device-compliance.md` — Enforcing access control based on device state
- `screenshots/` — Folder containing visual documentation
- `final-report.md` — Summary of configurations and security justifications

## How to Use This Repository

1. Clone this repository or fork it to your profile.
2. Follow each configuration guide under the respective `.md` files.
3. Review the final report to understand how all policies work together.
4. Use the content for your own documentation, lab practice, or portfolio.

## Security Concepts Applied

- Zero Trust Architecture
- Identity and Access Management (IAM)
- Multi-Factor Authentication (MFA)
- Conditional Access
- Endpoint Security and Compliance
- Risk-Based Sign-In Protection

## Future Enhancements

- Add Data Loss Prevention (DLP) policies
- Integrate Microsoft Defender for Endpoint
- Simulate phishing attack and document detection response
- Record a video walkthrough or publish a blog post

## Author

Erik [your last name or GitHub username]  
[Your LinkedIn URL or Portfolio Site]  
[Optional: Certification or Title, e.g., CompTIA Security+, Level 2 Technician]

