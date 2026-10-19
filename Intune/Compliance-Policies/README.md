# Windows Compliance Baseline

Production-ready Microsoft Intune Windows compliance policies designed to enforce device health, endpoint security, and Microsoft Defender for Endpoint risk requirements.

These compliance policies are intended for Microsoft Intune managed Windows devices and integrate with Conditional Access to enforce Zero Trust principles.

## Included Policies

| File | Description |
|--------|--------|
| Windows - Compliance - Device Health.json | Validates BitLocker, Secure Boot and Code Integrity |
| Windows - Compliance - Security.json | Validates Defender, Antivirus, Anti-Spyware and Firewall |
| Windows - Compliance - Security Intelligence.json | Validates Defender security intelligence updates |
| Windows - Compliance - MDE Risk.json | Validates Microsoft Defender for Endpoint risk score |

---

## Purpose

This compliance baseline helps organizations:

- Enforce device encryption
- Validate endpoint protection
- Verify signature currency
- Assess endpoint risk using Defender for Endpoint
- Support Conditional Access policies
- Implement Zero Trust controls

---

## Device Health

### Included Controls

- BitLocker Enabled
- Secure Boot Enabled
- Code Integrity Enabled

### Purpose

Ensures devices meet basic hardware and operating system security requirements before access is granted.

---

## Security

### Included Controls

- Microsoft Defender Enabled
- Antivirus Required
- Anti-Spyware Required
- Real-Time Protection Enabled
- Windows Firewall Required

### Purpose

Confirms endpoint security protections remain active and operational.

---

## Security Intelligence

### Included Controls

- Microsoft Defender Enabled
- Security Intelligence Up-To-Date

### Purpose

Ensures devices are protected by current threat definitions and malware signatures.

---

## Microsoft Defender for Endpoint Risk

### Included Controls

- Defender for Endpoint Integrated
- Maximum Device Risk Level: Medium

### Purpose

Leverages Microsoft Defender for Endpoint threat intelligence to identify compromised or high-risk devices.

---

## Conditional Access Integration

These policies are designed to work alongside Microsoft Entra Conditional Access policies:

- Require compliant device
- Require approved applications
- Block non-compliant devices
- Restrict access to unmanaged devices

---

## Technologies

- Microsoft Intune
- Microsoft Entra ID
- Conditional Access
- Microsoft Defender Antivirus
- Microsoft Defender for Endpoint
- Zero Trust
