# BitLocker & Personal Data Encryption (PDE) Baseline

Production-ready Microsoft Intune security baselines focused on securing Windows devices using:
- BitLocker Drive Encryption
- Personal Data Encryption (PDE)

These configurations are designed for modern Microsoft Intune managed environments using Microsoft Entra ID and Microsoft Defender.

---

# Included Policies

## BitLocker Baseline

This policy enables and configures BitLocker Drive Encryption for Windows devices.

### Key Features
- XTS-AES 256-bit encryption
- TPM-based protection
- Silent encryption support
- Recovery password rotation
- Entra ID recovery key backup
- Standard user encryption support
- Fixed drive encryption support
- Removable drive encryption support

### Recommended For
- Microsoft Entra ID Joined devices
- Hybrid Joined devices
- Corporate-owned Windows devices
- Microsoft Business Premium and above

---

## Personal Data Encryption (PDE)

This policy enables Microsoft Personal Data Encryption (PDE) to provide additional protection for user profile data.

### Protected Locations
- Desktop
- Documents
- Pictures

### Key Features
- User-based encryption protection
- Integrated with Windows security architecture
- Additional protection for sensitive user data
- Seamless user experience

---

# Requirements

## Licensing
Recommended:
- Microsoft 365 Business Premium
- Microsoft 365 E3/E5
- Microsoft Intune

## Operating System
- Windows 11 supported versions
- TPM 2.0 recommended

## Identity
- Microsoft Entra ID Joined
or
- Hybrid Entra ID Joined

---

# Files Included

| File | Description |
|---|---|
| `ZTBH - Windows - Security - BitLocker Baseline.json` | Main BitLocker encryption baseline policy |
| `ZTBH - Windows - Security - BitLocker PDE.json` | Personal Data Encryption (PDE) policy |

---

# Recommended Deployment Approach

1. Deploy to a pilot group first
2. Verify recovery keys are backing up correctly
3. Validate encryption status on test devices
4. Monitor Intune and Defender for issues
5. Expand deployment gradually

---

# Important Notes

- Always test policies before production deployment
- Ensure devices meet TPM and Windows requirements
- Review compliance and Conditional Access dependencies before rollout
- Some settings may require reboot or user sign-in refresh

---

# Related Technologies

- Microsoft Intune
- Microsoft Entra ID
- Microsoft Defender
- Windows Security
- Zero Trust Architecture

---

# Disclaimer

These policies are provided as example baselines and should be tested and reviewed before deployment into production environments.

The Zero Trust Blueprint Hub repository is intended to provide practical deployment examples and educational guidance for Microsoft security technologies.
