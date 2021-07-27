﻿---
description: Create a deployment for an automatic deployment rule.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: New-CMAutoDeploymentRuleDeployment
---

# New-CMAutoDeploymentRuleDeployment

## SYNOPSIS

Create a deployment for an automatic deployment rule.

## SYNTAX

### ByName (Default)
```
New-CMAutoDeploymentRuleDeployment [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>]
 [-AllowDownloadFromMicrosoftUpdate <Boolean>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-DisableOperationsManager <Boolean>] [-EnableDeployment <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-Name] <String>
 [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SuccessPercentage <Int32>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationOption>] [-UseUtc <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMAutoDeploymentRuleDeployment [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>]
 [-AllowDownloadFromMicrosoftUpdate <Boolean>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-DisableOperationsManager <Boolean>] [-EnableDeployment <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-Id] <Int32>
 [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SuccessPercentage <Int32>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationOption>] [-UseUtc <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMAutoDeploymentRuleDeployment [-AlertTime <Int32>] [-AlertTimeUnit <TimeUnitType>]
 [-AllowDownloadFromMicrosoftUpdate <Boolean>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>] [-DeadlineTimeUnit <TimeUnitType>]
 [-DisableOperationsManager <Boolean>] [-EnableDeployment <Boolean>]
 [-GenerateOperationsManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>] [-InputObject] <IResultObject>
 [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>] [-RequirePostRebootFullScan <Boolean>]
 [-SendWakeupPacket <Boolean>] [-SoftDeadlineEnabled <Boolean>] [-SuccessPercentage <Int32>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationOption>] [-UseUtc <Boolean>] [-VerboseLevel <VerboseLevelType>]
 [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMAutoDeploymentRuleDeployment** cmdlet creates a deployment for an automatic deployment rule (ADR).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a deployment for an automatic deployment rule by name

This command creates a deployment for the automatic deployment rule **TestDepRule01** and the **All Systems** collection.

```powershell
New-CMAutoDeploymentRuleDeployment -Name "TestDepRule01" -CollectionName "All Systems" -EnableDeployment $true -SendWakeupPacket $false -VerboseLevel OnlySuccessAndErrorMessages -UseUtc $false  -AvailableTime 7 -AvailableTimeUnit Days -DeadlineTime 7 -DeadlineTimeUnit Days -UserNotification DisplaySoftwareCenterOnly -AllowSoftwareInstallationOutsideMaintenanceWindow $false -AllowRestart $false -SuppressRestartServer  $false -SuppressRestartWorkstation $false -WriteFilterHandling $false -GenerateSuccessAlert $true -SuccessPercentage 10 -AlertTime 7 -AlertTimeUnit Days -DisableOperationsManager $false -GenerateOperationsManagerAlert $false -NoInstallOnRemote $false -NoInstallOnUnprotected $false -UseBranchCache $false
```

### Example 2: Create a deployment for an automatic deployment rule by object

This command gets the automatic deployment rule object named **TestDepRule02**. It then uses the pipeline operator to pass the object to **New-CMAutoDeploymentRuleDeployment**, which creates a deployment for automatic deployment rule **TestDepRule02** and the **All Systems** collection.

```powershell
Get-CMAutoDeploymentRule -Name "TestDepRule02" | New-CMAutoDeploymentRuleDeployment -CollectionName "All Systems" -EnableDeployment $true -SendWakeupPacket $false -VerboseLevel OnlySuccessAndErrorMessages -UseUtc $false -AvailableTime 7 -AvailableTimeUnit Days -DeadlineTime 7 -DeadlineTimeUnit Days -UserNotification DisplaySoftwareCenterOnly -AllowSoftwareInstallationOutsideMaintenanceWindow $false -AllowRestart $false -SuppressRestartServer $false -SuppressRestartWorkstation $false -WriteFilterHandling $false -GenerateSuccessAlert  $true -SuccessPercentage 10 -AlertTime 7 -AlertTimeUnit Days -DisableOperationsManager $false -GenerateOperationsManagerAlert $false -NoInstallOnRemote $false -NoInstallOnUnprotected $false -UseBranchCache $false
```

## PARAMETERS

### -AlertTime

Specifies the number of time units for the offset from the deadline.

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

### -AlertTimeUnit

Specifies the time unit type for the offset from the deadline.

```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDownloadFromMicrosoftUpdate

Starting in version 1906, use this parameter to set the following option on the **Download Settings** page of the ADR deployment settings: **If software updates are not available on distribution point in current, neighbor or site boundary groups, download content from Microsoft Updates**.


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

### -AllowRestart

Indicates whether a system restart is allowed to be performed outside of any defined maintenance windows when the installation deadline is reached.

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

### -AllowSoftwareInstallationOutsideMaintenanceWindow

Indicates whether software installation is allowed to be performed outside of any defined maintenance windows when the installation deadline is reached.

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

### -AllowUseMeteredNetwork

Starting in version 1906, use this parameter to set the following option on the **Download Settings** page of the ADR deployment settings: **Allow clients on a metered Internet connection to download content after the installation deadline, which might incur additionl costs**

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

### -AvailableImmediately

Indicates whether software updates are available to install as soon as possible after the rule is run.

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

### -AvailableTime

Specifies the number of time units for the software available time.

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

### -AvailableTimeUnit

Specifies the time unit type for the software available time.

```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection

Specifies a target collection object for the software update deployment. To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -CollectionId

Specifies the ID of the target collection for the software update deployment.

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

### -CollectionName

Specifies the name of the target collection for the software update deployment.

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

### -DeadlineImmediately

Indicates whether required software updates are installed as soon as possible when the deadline is reached.

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

### -DeadlineTime

Specifies the number of time units for the deadline.

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

### -DeadlineTimeUnit

Specifies the time unit type for the deadline.

```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableOperationsManager

Indicates whether Operations Manager alerts are disabled while software updates run.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisableOperationManager

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

### -EnableDeployment

Indicates whether to enable the deployment after this rule runs for the associated software group. If set to `$False`, manually deploy the software update group.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enable, EnabledAfterCreate, EnableAfterCreate

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

### -GenerateOperationsManagerAlert

Indicates whether Operations Manager alerts are generated when a software update installation fails.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: GenerateOperationManagerAlert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GenerateSuccessAlert

Indicates whether an alert is generated when this rule runs successfully.

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

### -Id

Specifies the ID of the automatic deployment rule to add this deployment to.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: AutoDeploymentID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies an automatic deployment rule object to add this deployment to. To obtain an automatic deployment rule object, use the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: AutoDeploymentRule

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of the automatic deployment rule to add this deployment to.

```yaml
Type: String
Parameter Sets: ByName
Aliases: AutoDeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoInstallOnRemote

Indicates whether to install software updates when the updates are not available on any remote distribution points.

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

### -NoInstallOnUnprotected

Indicates whether to install software updates when the updates are not available on any unprotected distribution points.

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

### -RequirePostRebootFullScan

Starting in version 1906, use this parameter to set the following option on the **User Experience** page of the ADR deployment settings: **If any update in this deployment requires a system restart, run updates deployment evaluation cycle after restart**.


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RunEvaluationAfterRestart

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeupPacket

Indicates whether to use Wake-on-LAN to wake up clients for required deployments.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableWakeOnLan

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftDeadlineEnabled

Starting in version 1906, use this parameter to set the following option on the **Deployment Schedule** page of the ADR deployment settings: **Delay enforcement of this deployment according to user preferences, up to the grace period defined in client settings**.


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DelayEnforcementAndUpToGracePeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuccessPercentage

Specifies the percent as an integer of client compliance. When client compliance falls below this percentage, an alert is generated.

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

### -SuppressRestartServer

Indicates whether a system restart is suppressed on servers when a software update requires a system restart to complete the installation process.

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

### -SuppressRestartWorkstation

Indicates whether a system restart is suppressed on workstations when a software update requires a system restart to complete the installation process.

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

### -UseBranchCache

Indicates whether clients are allowed to share content with other clients on the same subnet.

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

### -UserNotification

Specifies the notification behavior of the user visual experience.

```yaml
Type: UserNotificationOption
Parameter Sets: (All)
Aliases:
Accepted values: DisplayAll, DisplaySoftwareCenterOnly, HideAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtc

Indicates whether the schedule for this deployment is evaluated based upon Universal Coordinated Time (UTC).

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

### -VerboseLevel

Specifies how much state detail the clients report back for deployments created by this rule.

```yaml
Type: VerboseLevelType
Parameter Sets: (All)
Aliases:
Accepted values: OnlyErrorMessages, OnlySuccessAndErrorMessages, AllMessages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteFilterHandling

Indicates whether changes are committed at deadline or during a maintenance window (requires restarts). If set to `$False`, content is applied on the overlay and committed later.

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

### IResultObject#SMS_AdrDeploymentSettings
## NOTES

## RELATED LINKS

[Get-CMAutoDeploymentRuleDeployment](Get-CMAutoDeploymentRuleDeployment.md)

[Remove-CMAutoDeploymentRuleDeployment](Remove-CMAutoDeploymentRuleDeployment.md)

[Set-CMAutoDeploymentRuleDeployment](Set-CMAutoDeploymentRuleDeployment.md)
