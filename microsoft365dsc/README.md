Manages, configures, extracts and monitors Microsoft 365 tenant configurations

Download the Project here : 
- https://github.com/microsoft/Microsoft365DSC

Documentation is avalable here
- https://microsoft365dsc.com/

# Requirements 

- M365 tenant

  You need a tenant for test.

  You can use the developper program for testing: https://developer.microsoft.com/en-us/microsoft-365/profile

- Windows with PowerShell 5.1

# For DevOps Deploymnet
- DevOps tenant and project

  2 DevOps pipeline : 
  * to deploy config
  * to detect drift

- At least one Windows agent with PowerShell 5.1

- One Azure AD Application

- One Azure Keyvault


## DNS 

| DNS/URL | Usage  |
|---|---|
| www.powershellgallery.com  | Modules source  |
| microsoft365dsc.com | Main project page  |
| export.microsoft365dsc.com | Project page configuration generator |
| ps.compliance.protection.outlook.com | Connect to Security & Compliance PowerShell: https://learn.microsoft.com/en-us/powershell/exchange/connect-to-scc-powershell?view=exchange-ps |
| login.live.com | Sign-In to every Microsoft Services |
| aadcdn.msauth.net | Part of Microsoft content delivery network (CDN): https://learn.microsoft.com/en-us/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops&tabs=IP-V4 |
| login.microsoftonline.com | Microsoft 365 Login: https://learn.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-auth-code-flow |

## MODULES

| Module Name | Usage  |
|---|---|
| Microsoft365DSC  |  main module |
| ReverseDSC | dependency |
| DSCParser | dependency |
| ExchangeOnlineManagement | dependency |
| Microsoft.Graph.Applications | dependency |
| Microsoft.Graph.DeviceManagement | dependency |
| Microsoft.Graph.DeviceManagement.Administration | dependency |
| Microsoft.Graph.DeviceManagement.Enrolment | dependency |
| Microsoft.Graph.Devices.CorporateManagement | dependency |
| Microsoft.Graph.Groups | dependency |
| Microsoft.Graph.Identity.DirectoryManagement | dependency |
| Microsoft.Graph.Identity.Governance | dependency |
| Microsoft.Graph.Identity.SignIns | dependency |
| Microsoft.Graph.Planner | dependency |
| Microsoft.Graph.Teams | dependency |
| Microsoft.Graph.Users | dependency |
| Microsoft.Graph.Users.Actions | dependency |
| Microsoft.PowerApps.Administration.PowerShell | dependency |
| MicrosoftTeams | dependency |
| MSCloudLoginAssistant | dependency |
| PnP.PowerShell | dependency |
| Az.Resources | DevOps req. |
| Az.KeyVault | DevOps req. |

To install the required modules :
```
Install-Module Microsoft365DSC -Force
Install-Module ReverseDSC -Force
Update-M365DSCDependencies
    Installing XXXXXX version {A.B.CCC}
Install-Module Az.Resources, Az.KeyVault 
```

# Export configuration

## FIRST RUN: Local export Security & Compliance
Code generated from https://export.microsoft365dsc.com/#Security%20&%20Compliance

```
Export-M365DSCConfiguration -Components @("SCAuditConfigurationPolicy", "SCAutoSensitivityLabelPolicy", "SCAutoSensitivityLabelRule", "SCCaseHoldPolicy", "SCCaseHoldRule", "SCComplianceCase", "SCComplianceSearch", "SCComplianceSearchAction", "SCComplianceTag", "SCDeviceConditionalAccessPolicy", "SCDeviceConfigurationPolicy", "SCDLPCompliancePolicy", "SCDLPComplianceRule", "SCFilePlanPropertyAuthority", "SCFilePlanPropertyCategory", "SCFilePlanPropertyCitation", "SCFilePlanPropertyDepartment", "SCFilePlanPropertyReferenceId", "SCFilePlanPropertySubCategory", "SCLabelPolicy", "SCProtectionAlert", "SCRetentionCompliancePolicy", "SCRetentionComplianceRule", "SCRetentionEventType", "SCSensitivityLabel", "SCSupervisoryReviewPolicy", "SCSupervisoryReviewRule")
```