# Windows Firewall Baseline

Production-ready Microsoft Intune Windows Firewall baseline focused on securing Windows devices using Microsoft Defender Firewall across:
- Domain Profile
- Private Profile
- Public Profile

This configuration is designed for modern Microsoft Intune managed environments using Microsoft Entra ID and Microsoft Defender. :contentReference[oaicite:0]{index=0}

---

# Included Policy

| File | Description |
|---|---|
| `ZTBH - Windows - Security - Firewall Baseline.json` | Microsoft Defender Firewall baseline for Windows devices |

---

# Key Features

## Firewall Protection Enabled
Enables Microsoft Defender Firewall for:
- Domain networks
- Private networks
- Public networks

---

## Secure Inbound Protection
Configured with:
- Default inbound action = Block
- Default outbound action = Allow

This aligns with Zero Trust security principles by blocking unsolicited inbound traffic while allowing legitimate outbound communication.

---

## Firewall Logging Enabled

Logging is configured for:
- Dropped packets
- Ignored rules
- Successful connections

### Log File Locations

| Profile | Log File |
|---|---|
| Domain | `%systemroot%\system32\LogFiles\Firewall\DomainFirewall.log` |
| Private | `%systemroot%\system32\LogFiles\Firewall\PrivateFirewall.log` |
| Public | `%systemroot%\system32\LogFiles\Firewall\PublicFirewall.log` |

### Log Size
- Maximum log size: 1024 KB

---

## Stealth Mode Protection
Stealth mode protections are enabled to reduce device visibility on networks and improve protection against network scanning.

---

## Notification Suppression
Inbound firewall notifications are disabled to provide a cleaner user experience and reduce unnecessary prompts.

---

# Configured Security Behavior

| Setting | Configuration |
|---|---|
| Firewall Enabled | Domain / Private / Public |
| Default Inbound Action | Block |
| Default Outbound Action | Allow |
| Log Dropped Packets | Enabled |
| Log Ignored Rules | Enabled |
| Log Successful Connections | Enabled |
| Inbound Notifications | Disabled |
| Stealth Mode | Enabled |

---

# Requirements

## Licensing
Recommended:
- Microsoft 365 Business Premium
- Microsoft 365 E3/E5
- Microsoft Intune

---

## Operating System
- Windows 10
- Windows 11

---

## Identity Requirements
Supported scenarios:
- Microsoft Entra ID Joined
- Hybrid Entra ID Joined

---

# Recommended Deployment Approach

1. Deploy to a pilot group first
2. Validate required applications and network traffic
3. Review firewall logs for blocked traffic
4. Create required allow rules if necessary
5. Expand deployment gradually

---

# Recommended Companion Technologies

- Microsoft Defender for Endpoint
- Microsoft Intune
- Microsoft Entra ID
- Conditional Access
- Attack Surface Reduction (ASR)

---

# Important Notes

- Firewall rules may impact legacy applications or custom network traffic
- Always validate business-critical applications after deployment
- Review firewall logs during pilot deployments
- Additional allow rules may be required for certain applications or services

---

# Related Technologies

- Microsoft Defender Firewall
- Microsoft Intune
- Microsoft Defender for Endpoint
- Zero Trust Security
- Windows Security

---

# Disclaimer

These policies are provided as example baselines and should be tested and reviewed before deployment into production environments.

The Zero Trust Blueprint Hub repository is intended to provide practical deployment examples and educational guidance for Microsoft security technologies.
