# Multi-Factor Authentication Setup

## Objective

Enable Multi-Factor Authentication (MFA) for users in Microsoft Entra ID to secure identity access and reduce the risk of account compromise.

## Tools Used

- Microsoft Entra Admin Center
- Security Defaults and/or Per-User MFA configuration

## Steps

### 1. Access Entra Admin Center

- Go to https://entra.microsoft.com
- Navigate to **Users > All Users**
- Select a test user account

### 2. Enable MFA (Option 1: Security Defaults)

- Navigate to **Properties**
- Scroll to **Manage Security Defaults**
- Turn **Security Defaults** to **On**
- Confirm settings

### 3. Enable MFA (Option 2: Per-User MFA)

- Visit: https://account.activedirectory.windowsazure.com/UserManagement/MultifactorVerification.aspx
- Select a user and click **Enable**
- User will be prompted to complete MFA setup on next sign-in

## Screenshots

_Add screenshots to show each step visually._  
_Place them in the `screenshots/` folder and link them like this:_

`![Enable MFA](../screenshots/enable-mfa-step1.png)`

## Why This Matters

Multi-Factor Authentication significantly improves account security by requiring a second form of verification beyond just a password. It helps prevent unauthorized access even if credentials are compromised through phishing or brute force attacks.

## Reference

- [Microsoft: What is MFA](https://learn.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks)
