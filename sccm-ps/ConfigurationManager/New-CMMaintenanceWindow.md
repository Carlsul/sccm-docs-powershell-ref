﻿---
description: Creates a maintenance window for a collection.
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMMaintenanceWindow
---

# New-CMMaintenanceWindow

## SYNOPSIS
Creates a maintenance window for a collection.

## SYNTAX

### ByValue (Default)
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-InputObject] <IResultObject> [-IsEnabled <Boolean>] [-IsUtc <Boolean>]
 -Name <String> -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCollectionId
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-CollectionId] <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>] -Name <String>
 -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByCollectionName
```
New-CMMaintenanceWindow [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToSoftwareUpdateOnly]
 [-ApplyToTaskSequenceOnly] [-CollectionName] <String> [-IsEnabled <Boolean>] [-IsUtc <Boolean>] -Name <String>
 -Schedule <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMMaintenanceWindow** cmdlet creates a maintenance window for a collection.
Maintenance windows are periods of time reserved for write operations such as applying software updates, installing software, or configuring computer settings.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a maintenance window
```
PS XYZ:\> $MWSchedule = New-CMSchedule -DayOfWeek Friday -DurationCount 0 -DurationInterval Hours -RecurCount 1 -Start "10/12/2013 21:00:00"
PS XYZ:\> New-CMMaintenanceWindow -CollectionID "AAA0005D" -Name "MonthlySchedule" -Schedule $MWSchedule
```

The first command uses the **New-CMSchedule** cmdlet to create a schedule object, and then stores it in the $MWSchedule variable.

The second command creates a maintenance window named MonthlySchedule for the specified collection.
The maintenance window uses the schedule stored in the $MWSchedule variable.

## PARAMETERS

### -ApplyTo
```yaml
Type: MaintenanceWindowApplyTo
Parameter Sets: (All)
Aliases:
Accepted values: Any, SoftwareUpdatesOnly, TaskSequencesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToSoftwareUpdateOnly
Indicates that the maintenance window is used to apply software updates only.

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

### -ApplyToTaskSequenceOnly
Indicates that the maintenance window is used to apply task sequences only.

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

### -CollectionId
Specifies the ID of the collection that the maintenance window applies to.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases:

Required: True
Position: 0
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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection, Site

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled
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

### -IsUtc
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

### -Name
Specifies the name of the maintenance window.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MaintenanceWindowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **CMSchedule** object.
The schedule specifies when the maintenance window occurs.
To create a **CMSchedule** object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### IResultObject#SMS_ServiceWindow

## NOTES

## RELATED LINKS

[Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

[New-CMSchedule](New-CMSchedule.md)

[Remove-CMMaintenanceWindow](Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](Set-CMMaintenanceWindow.md)
