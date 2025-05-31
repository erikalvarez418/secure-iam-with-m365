# Risk-Based MFA Policy

## Objective

Create a Conditional Access policy that requires Multi-Factor Authentication (MFA) only when Microsoft Entra Identity Protection detects risky sign-in behavior. This ensures adaptive access control while maintaining user productivity.

## Tools Used

- Microsoft Entra Admin Center
- Microsoft Identity Protection (built into Entra ID P2 or M365 E5 trial)

## Why This Matters

Risk-based policies allow dynamic responses to potentially malicious behavior such as impossible travel, unfamiliar sign-ins, or atypical locations. Requiring MFA only when risk is detected reduces friction for users while increasing security posture.

## Prerequisites

- You must have **Entra ID P2** or a **Microsoft 365 Developer E5** tenant to access sign-in risk levels.
- Users must be licensed for Identity Protection.

## Steps

### 1. Access Conditional Access

- Go to: https://entra.microsoft.com
- Navigate to **Protection > Conditional Access**
- Click **+ New policy**

### 2. Configure Policy

- **Name:** Require MFA for Risky Sign-ins

#### Assignments
- **Users:** All users (or a test group)
- **Cloud apps:** All cloud apps

#### Conditions
- **Sign-in Risk:**
  - Select: Medium and above

#### Access Controls
- **Grant Access:**  
  - Require Multi-Factor Authentication

### 3. Enable Policy

- Set **Enable policy** to **On**
- Click **Create**

## Screenshots

_Include screenshots of:_
- The Conditional Access setup for risk-based MFA
- Selecting "Sign-in risk"
- Grant controls requiring MFA

Example:
`![Risk-Based MFA Settings](../screenshots/risk-based-mfa-settings.png)`

## Testing

- Simulate risky sign-ins by:
  - Signing in from a different country (via VPN)
  - Logging in from an incognito browser or unfamiliar device
- Check sign-in logs for risk detections under **Entra > Identity Protection > Risky sign-ins**

## Reference

- [Microsoft: Sign-in risk in Conditional Access](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-policy-risk)
- [Microsoft: Identity Protection overview](https://learn.microsoft.com/en-us/azure/active-directory/identity-protection/overview-identity-protection)
