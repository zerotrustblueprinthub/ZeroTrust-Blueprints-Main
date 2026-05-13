# Windows LAPS Baseline

Production-ready Microsoft Intune Windows LAPS baseline focused on securing local administrator accounts on Windows devices using:
- Automatic local administrator account management
- Randomized account naming
- Password rotation
- Secure password backup to Microsoft Entra ID

This configuration is designed for modern Microsoft Intune managed environments using Microsoft Entra ID and Microsoft Defender. :contentReference[oaicite:0]{index=0}

---

# Included Policy

| File | Description |
|---|---|
| `ZTBH - Windows - Identity - Windows LAPS.json` | Windows LAPS baseline for Intune-managed Windows devices |

---

# Key Features

## Automatic Local Administrator Management
Automatically creates and manages a dedicated local administrator account on Windows devices.

Features include:
- Automatic account creation
- Automatic account enablement
- Randomized account naming
- Secure password rotation

---

## Secure Password Backup
Passwords are securely backed up to:
- Microsoft Entra ID

This removes the need for shared local administrator passwords across devices.

---

## Password Rotation
Passwords automatically rotate every:
- 7 days

This helps reduce the risk of credential reuse and lateral movement attacks.

---

## Strong Password Protection
Configured with:
- Passphrase complexity
- Passphrase length of 10
- Fallback password length of 21 characters

Designed to improve resistance against password attacks.

---

## Randomized Local Administrator Naming
Automatically generates randomized local administrator account names using:
```text id="r3j5a0"
ZTBH_Local
