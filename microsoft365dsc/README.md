Manages, configures, extracts and monitors Microsoft 365 tenant configurations

Download the Project here : 
- https://github.com/microsoft/Microsoft365DSC

Documentation is avalable here
- https://microsoft365dsc.com/

# Requirements

## Powershell
Use Powershell 5.1

## Tenant 

You need a tenant for test.

You can use the developper program for testing: https://developer.microsoft.com/en-us/microsoft-365/profile

## DNS 

| DNS/URL | Usage  |
|---|---|
| www.powershellgallery.com  |   |
| microsoft365dsc.com |   |
| export.microsoft365dsc.com |   |
| ps.compliance.protection.outlook.com |   |
| browser.events.data.microsoft.com |   |
| login.live.com |   |
| aadcdn.msauth.net |   |
| login.microsoftonline.com |   |

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

To install the required modules :
```
Install-Module Microsoft365DSC -Force
Install-Module ReverseDSC -Force
Update-M365DSCDependencies
    Installing XXXXXX version {A.B.CCC}
```

# Export configuration

## FIRST RUN: export Security & Compliance
Code generated from https://export.microsoft365dsc.com/#Security%20&%20Compliance

```
Export-M365DSCConfiguration -Components @("SCAuditConfigurationPolicy", "SCAutoSensitivityLabelPolicy", "SCAutoSensitivityLabelRule", "SCCaseHoldPolicy", "SCCaseHoldRule", "SCComplianceCase", "SCComplianceSearch", "SCComplianceSearchAction", "SCComplianceTag", "SCDeviceConditionalAccessPolicy", "SCDeviceConfigurationPolicy", "SCDLPCompliancePolicy", "SCDLPComplianceRule", "SCFilePlanPropertyAuthority", "SCFilePlanPropertyCategory", "SCFilePlanPropertyCitation", "SCFilePlanPropertyDepartment", "SCFilePlanPropertyReferenceId", "SCFilePlanPropertySubCategory", "SCLabelPolicy", "SCProtectionAlert", "SCRetentionCompliancePolicy", "SCRetentionComplianceRule", "SCRetentionEventType", "SCSensitivityLabel", "SCSupervisoryReviewPolicy", "SCSupervisoryReviewRule")
```