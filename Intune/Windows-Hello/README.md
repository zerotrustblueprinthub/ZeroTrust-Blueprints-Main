# Windows Hello for Business Baseline

Production-ready Microsoft Intune Windows Hello for Business baseline focused on secure, passwordless authentication for Windows devices using:
- PIN sign-in
- Biometrics
- TPM-backed credential protection
- Cloud Trust authentication

This configuration is designed for modern Microsoft Intune managed environments using Microsoft Entra ID and Microsoft Defender. :contentReference[oaicite:0]{index=0}

---

# Included Policy

| File | Description |
|---|---|
| `ZTBH - Windows - Identity - Windows Hello for Business.json` | Windows Hello for Business Intune configuration baseline |

---

# Key Features

## Passwordless Authentication
Enables Windows Hello for Business to replace traditional passwords with:
- PIN authentication
- Facial recognition
- Fingerprint authentication

---

## TPM-Backed Security
Requires supported security hardware (TPM) to protect authentication credentials and improve resistance against credential theft attacks.

---

## Cloud Trust Support
Enables Cloud Trust authentication for on-premises resources without requiring traditional certificate deployment.

Useful for:
- Hybrid environments
- Modern authentication deployments
- Simplified Windows Hello deployments

---

## Enhanced Biometric Security
Includes:
- Enhanced anti-spoofing protection
- Enhanced Sign-in Security (ESS)
- Secure biometric authentication support

---

# Configured Settings

| Setting | Value |
|---|---|
| Allow Biometrics | Enabled |
| Enable PIN Recovery | Enabled |
| Minimum PIN Length | 8 |
| Maximum PIN Length | 14 |
| Require Security Device (TPM) | Enabled |
| Use Cloud Trust for On-Prem Authentication | Enabled |
| Use Windows Hello for Business | Enabled |
| Enhanced Sign-in Security | Enabled |
| Facial Recognition Anti-Spoofing | Enabled |

---

# Requirements

## Licensing
Recommended:
- Microsoft 365 Business Premium
- Microsoft 365 E3/E5
- Microsoft Intune
- Microsoft Entra ID P1 or above

---

## Operating System
- Windows 10
- Windows 11
- TPM 2.0 recommended

---

## Identity Requirements
Supported scenarios:
- Microsoft Entra ID Joined
- Hybrid Entra ID Joined

---

# Recommended Deployment Approach

1. Deploy to a pilot group first
2. Verify TPM availability on devices
3. Confirm Cloud Trust prerequisites are configured
4. Validate user sign-in experience
5. Expand deployment gradually

---

# Recommended Companion Technologies

- Microsoft Intune
- Microsoft Entra ID
- Microsoft Defender
- Conditional Access
- Cloud Kerberos Trust

---

# Important Notes

- Some older hardware may not fully support biometric security features
- Cloud Trust requires proper identity synchronization and configuration
- Always validate authentication workflows before broad rollout
- Test on pilot devices before production deployment

---

# Related Technologies

- Windows Hello for Business
- Microsoft Intune
- Microsoft Entra ID
- Zero Trust Security
- Passwordless Authentication
- Cloud Trust

---

# Disclaimer

These policies are provided as example baselines and should be tested and reviewed before deployment into production environments.

The Zero Trust Blueprint Hub repository is intended to provide practical deployment examples and educational guidance for Microsoft security technologies.
