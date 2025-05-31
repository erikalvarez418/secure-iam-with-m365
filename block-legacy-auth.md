# Block Legacy Authentication

## Objective

Block legacy authentication protocols (such as POP, IMAP, SMTP) that do not support modern security controls like MFA. These protocols are often used in password spray and brute force attacks.

## Tools Used

- Microsoft Entra Admin Center
- Conditional Access

## Why This Matters

Legacy authentication methods bypass MFA and are frequently targeted by attackers. Blocking these protocols helps reduce the organization’s attack surface and aligns with Zero Trust principles.

## Steps

### 1. Access Conditional Access

- Go to: https://entra.microsoft.com
- Navigate to **Protection > Conditional Access**
- Click **+ New policy**

### 2. Configure Policy

- **Name:** Block Legacy Authentication

#### Assignments
- **Users:** All users or a test group
- **Cloud apps:** All cloud apps (or select critical ones)

#### Conditions
- **Client Apps:**  
  - Enable this condition  
  - Select: **Other clients** and **Legacy authentication clients**

#### Access Controls
- **Grant:** Block access

### 3. Enable Policy

- Set **Enable policy** to **On**
- Click **Create**

## Screenshots

_Add screenshots showing the configuration for:_
- Selecting users and apps
- Enabling "Client Apps" condition
- Granting block access

Example:
`![Legacy Auth Settings](../screenshots/block-legacy-auth-client-apps.png)`

## Testing

- Try signing in to an email client that uses legacy auth (e.g., Outlook 2010 or IMAP client)
- Confirm that access is blocked

## Reference

- [Microsoft: Block legacy authentication](https://learn.microsoft.com/en-us/azure/active-directory/conditional-access/block-legacy-authentication)
