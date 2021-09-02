---
description: Creates a Configuration Manager configuration item.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: New-CMConfigurationItem
---

# New-CMConfigurationItem

## SYNOPSIS

Creates a Configuration Manager configuration item.

## SYNTAX

### NewChild (Default)
```
New-CMConfigurationItem [-Category <String[]>] [-Description <String>] -Name <String>
 -ParentConfigurationItem <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### New
```
New-CMConfigurationItem [-Category <String[]>] -CreationType <CICreationType> [-Description <String>]
 -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **New-CMConfigurationItem** cmdlet creates a configuration item in Configuration Manager.
Create configuration items to define configurations that you want to manage and assess for compliance on devices.

You can specify the *ParentConfigurationItem* parameter to create a child configuration item.
Child configuration items in Configuration Manager are copies of configuration items that retain a relationship to the original configuration item; therefore, they inherit the original configuration from the parent configuration item.
You cannot create child configuration items for mobile devices.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a configuration item

```powershell
PS XYZ:\> New-CMConfigurationItem -CreationType MobileDevice -Name "MD_Config88"
```

This command creates a configuration item for mobile devices named MD_Config88.

## PARAMETERS

### -Category

Specifies an array of localized names of the categories to which the configuration item belongs.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreationType

Specifies the type of configuration item.
The acceptable values for this parameter are:

- MacOS
- MobileDevice
- None
- WindowsApplication
- WindowsOS

```yaml
Type: CICreationType
Parameter Sets: New
Aliases:
Accepted values: None, WindowsApplication, WindowsOS, MacOS, MobileDevice

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description for a configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

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

### -Name

Specifies a name for the configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentConfigurationItem

Specifies a parent **CMConfigurationItem** object.
To obtain a **CMConfigurationItem** object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: NewChild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### IResultObject#SMS_ConfigurationItem
## NOTES

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](/mem/configmgr/compliance/understand/ensure-device-compliance)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
