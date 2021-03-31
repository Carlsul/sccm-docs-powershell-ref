﻿---
description: Modifies a software update point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareUpdatePointComponent
---

# Set-CMSoftwareUpdatePointComponent

## SYNOPSIS
Modifies a software update point.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableSynchronization <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] [-NonFeatureUpdateMaxRuntimeMins <Int32>] [-PassThru]
 [-RemoveCompany <String[]>] [-RemoveLanguageSummaryDetail <String[]>] [-RemoveLanguageUpdateFile <String[]>]
 [-RemoveProduct <String[]>] [-RemoveProductFamily <String[]>] [-RemoveUpdateClassification <String[]>]
 [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>] [-SiteCode <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableSynchronization <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] -Name <String> [-NonFeatureUpdateMaxRuntimeMins <Int32>]
 [-PassThru] [-RemoveCompany <String[]>] [-RemoveLanguageSummaryDetail <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-RemoveProduct <String[]>] [-RemoveProductFamily <String[]>]
 [-RemoveUpdateClassification <String[]>] [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdatePointComponent [-AddCompany <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-AddLanguageUpdateFile <String[]>] [-AddProduct <String[]>] [-AddProductFamily <String[]>]
 [-AddUpdateClassification <String[]>] [-ContentFileOption <ContentFileOptions>] [-DefaultWsusServer <String>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-EnableManualCertManagement <Boolean>]
 [-EnableSyncFailureAlert <Boolean>] [-EnableSynchronization <Boolean>] [-EnableThirdPartyUpdates <Boolean>]
 [-FeatureUpdateMaxRuntimeMins <Int32>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-ImmediatelyExpireSupersedenceForFeature <Boolean>] -InputObject <IResultObject>
 [-NonFeatureUpdateMaxRuntimeMins <Int32>] [-PassThru] [-RemoveCompany <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-RemoveLanguageUpdateFile <String[]>] [-RemoveProduct <String[]>]
 [-RemoveProductFamily <String[]>] [-RemoveUpdateClassification <String[]>]
 [-ReportingEvent <ReportingEventType>] [-Schedule <IResultObject>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>] [-WaitMonth <Int32>]
 [-WaitMonthForFeature <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdatePointComponent** cmdlet modifies a software update point.
A software update point component interacts with a Windows Server Update Services (WSUS) server to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

You can specify a software update point to modify by name, by site code, or by using the [Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a software update point
```
PS XYZ:\> $CIObj = Get-CMSoftwareUpdatePointComponent -SiteSystemServerName "Contoso-SiteSysSrv.Western.Contoso.com"
PS XYZ:\> Set-CMSoftwareUpdatePointComponent -InputObject $CIObj
```

The first command retrieves a software update point component object on the server named Contoso-SiteSysSrv.TSQA.Contoso.com.
The command stores the object in the **$CIObj** variable.

The second command modifies the software update point component in **$CIObj**.

## PARAMETERS

### -AddCompany
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageSummaryDetail
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet adds these languages to the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProduct
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProductFamily
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet adds these classifications to the classifications supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentFileOption
```yaml
Type: ContentFileOptions
Parameter Sets: (All)
Aliases:
Accepted values: FullFilesOnly, ExpressForWindows10Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultWsusServer
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCallWsusCleanupWizard
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableManualCertManagement
Starting in version 1910, use this parameter to enable or disable manual management of the WSUS signing certificate for third-party updates.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSyncFailureAlert
Indicates whether Configuration Manager creates an alert when synchronization fails on a site.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSynchronization
Indicates whether this site automatically synchronizes updates according to a schedule.
Specify a schedule by using the *Schedule* parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableThirdPartyUpdates
Starting in version 1910, use this parameter to enable or disable the following option on the **Third Party Updates** tab of the software update point component properties: **Enable third-party software updates**.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FeatureUpdateMaxRuntimeMins
Starting in 1910, use this parameter to configure the following setting on the **Maximum Run Time** tab of the software update point component properties: **Maximum run time for Windows feature updates (minutes)**.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImmediatelyExpireSupersedence
Indicates whether a software update expires immediately after another update supersedes it or after a specified period of time.
If you specify a value of $False for this parameter, specify the number of months to wait for expiration by using the *WaitMonth* parameter.

System Center 2016 Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ImmediatelyExpireSupersedenceForNonFeature

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImmediatelyExpireSupersedenceForFeature
{{ Fill ImmediatelyExpireSupersedenceForFeature Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update point component object.
To obtain a software update point component object, use the [Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Site, SiteComponent

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a site system server in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonFeatureUpdateMaxRuntimeMins
Starting in 1910, use this parameter to configure the following setting on the **Maximum Run Time** tab of the software update point component properties: **Maximum run time for Office 365 updates and non-feature updates for Windows (minutes)**.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCompany
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageSummaryDetail
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet removes these languages from the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProduct
Specifies an array of products, as strings.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProductFamily
Specifies an array of product families, as strings.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet removes these classifications from the classifications supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingEvent
Specifies whether to create event messages for WSUS reporting for status reporting events or for all reporting events.
The acceptable values for this parameter are:

- CreateAllWsusReportingEvents
- CreateOnlyWsusStatusReportingEvents
- DoNotCreateWsusReportingEvents

```yaml
Type: ReportingEventType
Parameter Sets: (All)
Aliases:
Accepted values: DoNotCreateWsusReportingEvents, CreateOnlyWsusStatusReportingEvents, CreateAllWsusReportingEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **Schedule** object.
Configuration Manager can synchronize updates according this schedule if you specify a value of $True for the *EnableSynchronization* parameter.
To obtain a **Schedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SynchronizeAction
Specifies a source for synchronization for this software update point.
The acceptable values for this parameter are:

- DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource
- SynchronizeFromAnUpstreamDataSourceLocation
- SynchronizeFromMicrosoftUpdate

If you select a value of SynchronizeFromAnUpstreamDataSourceLocation, specify the data source location by using the **UpstreamSourceLocation** parameter.

```yaml
Type: SynchronizeActionType
Parameter Sets: (All)
Aliases:
Accepted values: SynchronizeFromMicrosoftUpdate, SynchronizeFromAnUpstreamDataSourceLocation, DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpstreamSourceLocation
Specifies an upstream data location as a URL.
To use this location, specify a value of SynchronizeFromAnUpstreamDataSourceLocation for the *SynchronizeAction* parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitMonth
Specifies how long, in months, to wait before a software update expires after another update supersedes it.
Specify a value of $True for the *ImmediatelyExpireSupersedence* parameter for software updates to expire immediately.

Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WaitMonthForNonFeature

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitMonthForFeature
{{ Fill WaitMonthForFeature Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_Component

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md)

[New-CMSchedule](New-CMSchedule.md)

[Set-CMCollectionMembershipEvaluationComponent](Set-CMCollectionMembershipEvaluationComponent.md)

[Set-CMEmailNotificationComponent](Set-CMEmailNotificationComponent.md)

[Set-CMManagementPointComponent](Set-CMManagementPointComponent.md)

[Set-CMStatusReportingComponent](Set-CMStatusReportingComponent.md)

