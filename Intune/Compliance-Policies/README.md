# Windows Device Compliance

Microsoft Intune compliance policies designed to evaluate Windows device health, endpoint protection, security intelligence, and Microsoft Defender for Endpoint device risk.

These policies can be used with Microsoft Entra Conditional Access to require Windows devices to meet defined security requirements before accessing organisational resources.

> **Important:** Review and test all policies in a pilot group before deploying them in a production environment.

## Included Files

| File | Description |
|------|-------------|
| ZTBH - Windows - Compliance - Device Health.json | Validates BitLocker, Secure Boot, and Code Integrity requirements. |
| ZTBH - Windows - Compliance - Security.json | Validates Microsoft Defender Antivirus, Real-Time Protection, Anti-Spyware, and Windows Firewall. |
| ZTBH - Windows - Compliance - Security Intelligence.json | Validates that Microsoft Defender is enabled and security intelligence is current. |
| ZTBH - Windows - Compliance - MDE Risk.json | Uses Microsoft Defender for Endpoint device-risk signals to evaluate compliance. |
| General Compliance Notification.json | Notification template used to inform users when a device has a compliance issue. |

---

## Policy Overview

The compliance configuration is separated into four policies. This makes each area easier to test, assign, troubleshoot, and update independently.

### ZTBH - Windows - Compliance - Device Health

Validates core Windows device-health protections.

#### Included controls

- BitLocker enabled
- Secure Boot enabled
- Code Integrity enabled

#### Purpose

Helps ensure that managed Windows devices use encryption, trusted boot protection, and operating-system integrity controls.

---

### ZTBH - Windows - Compliance - Security

Validates the status of the main Windows endpoint security protections.

#### Included controls

- Microsoft Defender enabled
- Real-Time Protection enabled
- Antivirus required
- Anti-Spyware required
- Windows Firewall required

#### Purpose

Helps ensure that endpoint protection and Windows Firewall remain enabled on managed Windows devices.

---

### ZTBH - Windows - Compliance - Security Intelligence

Validates Microsoft Defender and its security intelligence status.

#### Included controls

- Microsoft Defender enabled
- Security intelligence signatures must not be out of date

#### Purpose

Helps ensure that devices use current Microsoft Defender security intelligence when evaluating compliance.

---

### ZTBH - Windows - Compliance - MDE Risk

Uses Microsoft Defender for Endpoint risk information as part of the Intune compliance assessment.

#### Included controls

- Microsoft Defender for Endpoint device-risk integration enabled
- Maximum permitted device-risk level: Medium

#### Purpose

Allows Intune to mark a device as non-compliant when its Microsoft Defender for Endpoint risk level exceeds the configured threshold.

---

## Compliance Notification

### General Compliance Notification

The included notification template can be linked to an Intune compliance policy action to inform users when a device has a compliance issue.

The template includes:

- Organisation name and logo
- Organisation contact information
- Company Portal link
- User name
- Device name
- Operating-system version
- Intune device ID
- Guidance to open Company Portal and select **Check access**
- IT Service Desk contact details

The default language configured in the exported template is English (United Kingdom), identified as `en-gb`.

---

## Conditional Access Integration

These compliance policies can support Microsoft Entra Conditional Access controls such as:

- Require device to be marked as compliant
- Block access from non-compliant devices
- Restrict access from unmanaged devices
- Combine device compliance with additional grant controls

Conditional Access policies are not included in this folder.

---

## Recommended Deployment Approach

Before production deployment:

1. Import or recreate the required policies in Microsoft Intune.
2. Review every imported setting.
3. Confirm that Microsoft Defender for Endpoint integration is configured before using the MDE Risk policy.
4. Assign the policies to a small pilot group.
5. Monitor compliance results and identify devices that cannot meet the requirements.
6. Test the notification template and remediation guidance.
7. Configure appropriate grace periods before enforcing access restrictions.
8. Expand assignments only after pilot testing is complete.

---

## Repository Structure

```text
Compliance-Policies
├── README.md
├── ZTBH - Windows - Compliance - Device Health.json
├── ZTBH - Windows - Compliance - Security.json
├── ZTBH - Windows - Compliance - Security Intelligence.json
├── ZTBH - Windows - Compliance - MDE Risk.json
└── General Compliance Notification.json
