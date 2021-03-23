﻿---
description: Gets a Configuration Manager task sequence step condition.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Get-CMTaskSequenceStepCondition
---

# Get-CMTaskSequenceStepCondition

## SYNOPSIS

Gets a Configuration Manager task sequence step condition.

## SYNTAX

```
Get-CMTaskSequenceStepCondition -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMTaskSequenceStepCondition** cmdlet gets task sequence condition object(s) in a task sequence group or step.  The cmdlet supports pipeline from a task sequence group or step object.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>$ReferencedTaskSequence | Get-CMTaskSequenceGroup -StepName $gpName | Get-CMTaskSequenceStepCondition
```

The command gets the task sequence condition objects from a task sequence group with a specific name.

## PARAMETERS

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

Specifies a task sequence step object.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: TaskSequenceStep

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_TaskSequence_Condition

### IResultObject#SMS_TaskSequence_Condition

## NOTES

## RELATED LINKS

[Add-CMTaskSequenceStep](./Add-CMTaskSequenceStep.md)

[Get-CMTaskSequenceStep](./Get-CMTaskSequenceStep.md)

[Remove-CMTaskSequenceStep](./Remove-CMTaskSequenceStep.md)

[Get-CMTaskSequenceGroup](./Get-CMTaskSequenceGroup.md)
