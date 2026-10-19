# Windows Compliance Baseline

Production-ready Microsoft Intune compliance policies designed to enforce device health, endpoint security, and Microsoft Defender for Endpoint risk requirements.

These policies are intended for Microsoft Intune managed Windows devices and integrate with Microsoft Entra Conditional Access to support Zero Trust security principles.

## Included Policies

| File | Description |
|--------|--------|
| ZTBH - Windows - Compliance - Device Health.json | Validates device encryption and platform security features. |
| ZTBH - Windows - Compliance - Security.json | Validates endpoint security and protection services. |
| ZTBH - Windows - Compliance - Security Intelligence.json | Validates Microsoft Defender security intelligence updates. |
| ZTBH - Windows - Compliance - MDE Risk.json | Validates Defender for Endpoint device risk levels. |

---

## Purpose

This compliance baseline helps organizations:

- Enforce device encryption
- Validate endpoint protection
- Verify security intelligence currency
- Assess endpoint risk using Defender for Endpoint
- Support Conditional Access requirements
- Implement Zero Trust controls

---

## ZTBH - Windows - Compliance - Device Health

### Included Controls

- BitLocker Enabled
- Secure Boot Enabled
- Code Integrity Enabled

### Purpose

Ensures devices meet core security requirements by validating device encryption, trusted boot protection, and operating system integrity.

---

## ZTBH - Windows - Compliance - Security

### Included Controls

- Microsoft Defender Enabled
- Real-Time Protection Enabled
- Antivirus Required
- Anti-Spyware Required
- Windows Firewall Required

### Purpose

Ensures security protections remain active and healthy, reducing the risk of malware, unauthorized access, and endpoint compromise.

---

## ZTBH - Windows - Compliance - Security Intelligence

### Included Controls

- Microsoft Defender Enabled
- Security Intelligence Signatures Current

### Purpose

Verifies that Microsoft Defender receives current threat intelligence and malware definition updates.

---

## ZTBH - Windows - Compliance - MDE Risk

### Included Controls

- Microsoft Defender for Endpoint Integration
- Maximum Device Risk Level: Medium

### Purpose

Uses Microsoft Defender for Endpoint risk assessments to identify compromised or suspicious devices and enforce risk-based compliance.

---

## Conditional Access Integration

These policies are designed to work alongside Microsoft Entra Conditional Access policies, including:

- Require compliant device
- Require approved applications
- Block non-compliant devices
- Restrict access to unmanaged devices
- Enforce Zero Trust access controls

---

## Technologies

- Microsoft Intune
- Microsoft Entra ID
- Conditional Access
- Microsoft Defender Antivirus
- Microsoft Defender for Endpoint
- Windows Security
- Zero Trust Security
