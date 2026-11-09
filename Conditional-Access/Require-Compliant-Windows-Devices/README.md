
# CA01 – Windows – Require Compliance

## Overview

This Conditional Access policy is designed to require Windows devices to be compliant with Microsoft Intune before accessing protected Microsoft 365 resources.

The policy builds on the Windows Device Compliance configuration covered in the Zero Trust Blueprint Hub series.

By combining Microsoft Intune Device Compliance with Microsoft Entra Conditional Access, organisations can restrict access to resources based on the compliance status of their devices.

## Policy Configuration

| Setting | Configuration |
|---------|---------------|
| Policy Name | CA01 - Windows - Require Compliance |
| Platform | Windows |
| Users | Configure based on your organisation's requirements |
| Target Resources | Configure based on your organisation's requirements |
| Grant Control | Require device to be marked as compliant |
| Policy State | Report-only recommended for initial deployment |

**Note:** Review the supplied JSON to confirm the actual assignments, exclusions and conditions before deployment.

## Prerequisites

Before deploying this policy, ensure:

- Microsoft Entra ID P1 licensing is available.
- Microsoft Intune is configured.
- Windows devices are enrolled in Intune.
- A Windows Device Compliance policy has been configured and assigned.
- Devices are successfully reporting their compliance status.
- Emergency access accounts are configured and excluded from Conditional Access policies where appropriate.

## Deployment Recommendations

1. Download the `CA01 - Windows - Require Compliance.json` file.
2. Review the policy configuration and tenant-specific identifiers.
3. Import or recreate the policy in Microsoft Entra Conditional Access.
4. Configure the appropriate user and group assignments.
5. Review excluded accounts, particularly emergency access accounts.
6. Start with the policy in **Report-only** mode.
7. Review Microsoft Entra sign-in logs to evaluate the policy's impact.
8. Test access from compliant and non-compliant Windows devices.
9. Once testing is successful, enable the policy for your intended users.

## Testing and Validation

After deploying the policy, use Microsoft Entra sign-in logs to review Conditional Access results.

**Compliant Device:**
- The device meets the configured Intune compliance requirements.
- Access is permitted, provided all other applicable Conditional Access requirements are satisfied.

**Non-Compliant Device:**
- The device does not meet the required compliance standards.
- Access is blocked when the policy is enabled and applicable.

**Unmanaged Device:**
- The device is not enrolled in Intune and cannot satisfy the compliant-device requirement.
- Access is blocked when the policy is enabled and applicable.

When testing browser access, ensure the browser supports passing device identity to Microsoft Entra ID. Otherwise, a compliant device may still fail the compliance requirement.

## Important Considerations

- Always test Conditional Access policies before enabling enforcement.
- Use Report-only mode to identify potential access issues.
- Ensure emergency access accounts are excluded.
- Consider how administrator accounts access Microsoft 365 resources, particularly when using separate administrative accounts.
- Review browser compatibility and device identity requirements.
- Review the impact on users accessing resources from unmanaged devices.
- Confirm the policy targets the intended resources and users.

## Related Configuration

This policy works alongside the Windows Device Compliance configuration available in the Zero Trust Blueprint Hub repository.

[Windows Device Compliance Policies](../../Intune/Compliance-Policies/)

## Disclaimer

These configurations are provided for educational purposes as part of the Zero Trust Blueprint Hub series.

Always review, customise and test policies before deploying them into a production environment.
