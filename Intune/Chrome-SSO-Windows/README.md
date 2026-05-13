# Chrome Microsoft SSO Extension Baseline

Production-ready Microsoft Intune Google Chrome Enterprise policy focused on enabling seamless Microsoft 365 authentication within Google Chrome using the Microsoft Single Sign-On extension.

This configuration is designed for modern Microsoft Intune managed environments using Microsoft Entra ID and Microsoft 365 services. :contentReference[oaicite:0]{index=0}

---

# Included Policy

| File | Description |
|---|---|
| `ZTBH - Windows - Browser - Chrome Microsoft SSO Extension.json` | Automatically installs the Microsoft Single Sign-On extension for Google Chrome |

---

# Purpose

Google Chrome does not natively support the same seamless Microsoft authentication experience available in Microsoft Edge.

This policy automatically installs the Microsoft Single Sign-On extension to improve:
- Microsoft 365 authentication
- Entra ID authentication
- Single Sign-On (SSO)
- User sign-in experience

---

# Key Features

## Automatic Extension Installation
Automatically installs the Microsoft Single Sign-On extension in Google Chrome using Intune policy configuration.

### Installed Extension ID
```text id="5d2c4w"
ppnbnpeolgkicgegkbkbjmhlideopiji
