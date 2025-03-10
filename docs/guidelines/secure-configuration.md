# Secure Configuration Assessment Guideline

This guideline is intended to define a simple approach to ongoing monitoring and assurance of secure configuration of common tools and platforms.

## Email, File sharing and Endpoint configuration monitoring

The standard recommended actions within [Microsoft Defender](https://security.microsoft.com/securescore?viewid=actions) should be reviewed and exported each month and retained for 12 months.

### Enhanced validation of cloud service configuration

A backup of tenant configuration should be taken each month with [Microsoft365DSC - Your Cloud Configuration](https://microsoft365dsc.com) and archived to a Git repository or equivalent VCS tool that allows monitoring of configuration drift.

A tool to review tenant configuration such as the [CISA ScubaGear M365 Secure Configuration Baseline Assessment Tool](https://github.com/cisagov/ScubaGear) should be run against all tenants at least quarterly with results reviewed and retained for 12 months to guide policy remediations and improvements.

![Microsoft365DSC Export UI](https://microsoft365dsc.com/Images/ExportUI.png)
![SCuBA Architecture diagram](https://github.com/cisagov/ScubaGear/raw/main/images/scuba-architecture.png)

### Enhanced validation of endpoint configuration

The [ACSC’s Cyber Toolbox](https://www.cyber.gov.au/about-us/news/essential-eight-assessment-guidance-package) is comprised of the Essential Eight Maturity Verification Tool (E8MVT) and the Application Control Verification Tool (ACVT) which should be run against a sampling of endpoints on at least a quarterly basis with results reviewed and retained for 12 months to guide policy remediations and improvements.

## Infrastructure (public cloud and on-premise compute and storage) configuration monitoring

The standard recommended actions within CSPM tools such as [Microsoft Defender for Cloud](https://portal.azure.com/#view/Microsoft_Azure_Security/SecurityMenuBlade/~/5)  and [AWS Security Hub](https://aws.amazon.com/security-hub/) should be reviewed and exported each month and retained for 12 months. It is strongly recommended to ensure checks are configured against the ACSC ISM and NIST CSF (SP 800-53 R5) using compliance dashboards:

- [Microsoft Defender for Cloud Compliance Dashboard](https://learn.microsoft.com/en-us/azure/defender-for-cloud/update-regulatory-compliance-packages)
- [Deploying a Conformance Pack Using the AWS Config Console](https://docs.aws.amazon.com/config/latest/developerguide/conformance-pack-console.html)

![Defender for Cloud Compliance Dashboard](https://learn.microsoft.com/en-us/azure/defender-for-cloud/media/concept-regulatory-compliance/compliance-dashboard.png)
![AWS Security Services](https://docs.aws.amazon.com/images/prescriptive-guidance/latest/security-reference-architecture/images/security-tooling-acct.png)

## Addressing Microsoft 365 cloud service risks

Organisations with Microsoft 365 premium or enterprise licencing should at a minimum undertake the following basics:

- Enable security defaults in Azure Active Directory. Microsoft has published [guidance on enabling Security defaults](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/concept-fundamentals-security-defaults#enabling-security-defaults). 
- Enrol your compatible devices in Intune. Microsoft has published guidance on [enrolling Windows devices in Intune](https://docs.microsoft.com/en-us/mem/intune/enrollment/windows-enrollment-methods).

![Security defaults](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/security-defaults/security-defaults-entra-admin-center.png)
![Intune enrollment](https://learn.microsoft.com/en-us/mem/intune/fundamentals/media/deployment-guide-enroll/deployment-plan-enroll.png)

This subsequently enables straightforward implementation of the [ACSCs Essential Eight](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/essential-eight) Microsoft 365 [Cloud Security Guides](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guides) listed below for reference:

- [Application control](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-application-control)
- [Patch applications](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-patch-applications)
- [Configure macro settings](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-configure-macro-settings)
- [User application hardening](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-user-application-hardening)
- [Restrict administrative privileges](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-restrict-administrative-privileges)
- [Patch operating systems](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-patch-operating-system)
- [Multi-factor authentication](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-multi-factor-authentication)
- [Regular backups](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/small-business-cyber-security/small-business-cloud-security-guide/technical-example-regular-backups)
