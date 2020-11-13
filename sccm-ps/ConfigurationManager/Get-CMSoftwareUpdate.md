﻿---
description: Gets a software update.
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareUpdate
---

# Get-CMSoftwareUpdate

## SYNOPSIS
Gets a software update.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdate [-ArticleId <String>] [-BulletinId <String>] [-Category <IResultObject[]>]
 [-CategoryName <String[]>] [-DatePostedMax <DateTime>] [-DatePostedMin <DateTime>]
 [-DateRevisedMax <DateTime>] [-DateRevisedMin <DateTime>] [-EulaExist <Boolean>] [-Fast] [-IncludeUpgrade]
 [-IsContentProvisioned <Boolean>] [-IsDeployed <Boolean>] [-IsExpired <Boolean>] [-IsLatest <Boolean>]
 [-IsOfflineServiceable <Boolean>] [-IsSuperseded <Boolean>] [-IsUserDefined <Boolean>] [-Name <String>]
 [-OnlyExpired] [-Severity <CustomSeverityType>] [-Vendor <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdate [-Fast] -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroup
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroupIdMandatory
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroupId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUpdateGroupNameMandatory
```
Get-CMSoftwareUpdate [-Fast] -UpdateGroupName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdate** cmdlet gets one or more software updates.
Clients receive a software update object when manually or automatically deploying a software update.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get software updates that have been downloaded
```
PS XYZ:\> Get-CMSoftwareUpdate -IsContentProvisioned $True
```

This command gets all software updates that have been downloaded.

### Example 2: Get software updates by update group
```
PS XYZ:\> Get-CMSoftwareUpdateGroup -Name "TestSUgroup10" | Get-CMSoftwareUpdate
```

This command gets the software update group object named TestSUgroup10 and uses the pipeline operator to pass the object to **Get-CMSoftwareUpdate**, which gets all software updates for the software update group object.

## PARAMETERS

### -ArticleId
Specifies the article ID of a software update.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BulletinId
Specifies the bulletin ID of a software update.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Category
Specifies the category of a software update.
To obtain a category object, use the Get-CMSoftwareUpdateCategory cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CategoryName
Specifies an array of category names for software updates.

```yaml
Type: String[]
Parameter Sets: SearchByName
Aliases: CategoryNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatePostedMax
Specifies the latest date that a software update was released.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatePostedMin
Specifies the earliest date that a software update was released.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateRevisedMax
Specifies the latest date that a software update was revised.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateRevisedMin
Specifies the earliest date that a software update was revised.

```yaml
Type: DateTime
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -EulaExist
```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases: EulaExists

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Id
Specifies the ID of a software update.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: SearchByName
Aliases: IncludeUpgrades

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsContentProvisioned
Indicates whether the software update is downloaded.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsDeployed
Indicates whether the software update is deployed.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsExpired
Indicates whether the software update has expired.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsLatest
Indicates whether the software update is the latest version.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsOfflineServiceable
Indicates whether the software update is offline-serviceable.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSuperseded
Indicates whether the software update is superseded.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsUserDefined
Indicates whether the software update is user-defined.

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a software update.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OnlyExpired
Indicates that the cmdlet only searches for expired software updates.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Severity
Specifies the severity of software update.
Valid values are:

- None
- Low
- Moderate
- Important
- Critical

```yaml
Type: CustomSeverityType
Parameter Sets: SearchByName
Aliases:
Accepted values: None, Low, Moderate, Important, Critical

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateGroup
Specifies a software update group object.
To obtain an update group object, use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByUpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UpdateGroupId
Specifies an array of IDs of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByUpdateGroupIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateGroupName
Specifies an array of names of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByUpdateGroupNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Vendor
{{ Fill Vendor Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_SoftwareUpdate

### IResultObject#SMS_SoftwareUpdate

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)

[Set-CMSoftwareUpdate](Set-CMSoftwareUpdate.md)

[Sync-CMSoftwareUpdate](Sync-CMSoftwareUpdate.md)


