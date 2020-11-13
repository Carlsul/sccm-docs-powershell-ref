﻿---
description: Removes an item from the Asset Intelligence catalog.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMAssetIntelligenceCatalogItem
---

# Remove-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Removes an item from the Asset Intelligence catalog.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAssetIntelligenceCatalogItem [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAssetIntelligenceCatalogItem -CategoryName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAssetIntelligenceCatalogItem [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAssetIntelligenceCatalogItem** cmdlet removes software categories, software families, and custom software labels from the Asset Intelligence catalog in Configuration Manager.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a catalog item by category name
```
PS XYZ:\> Remove-CMAssetIntelligenceCatalogItem -CategoryName "Database Tools"
```

This command removes the category named Database Tools from the Asset Intelligence catalog.

## PARAMETERS

### -CategoryName
Specifies the name of a category, family, or label in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies an array of IDs of asset intelligence catalog items.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an Asset Intelligence catalog item.
To get an Asset Intelligence catalog item, use the Get-CMAssetIntelligenceCatalogItem cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
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

### System.Object
## NOTES

## RELATED LINKS

[Get-CMAssetIntelligenceCatalogItem](Get-CMAssetIntelligenceCatalogItem.md)

[New-CMAssetIntelligenceCatalogItem](New-CMAssetIntelligenceCatalogItem.md)

[Set-CMAssetIntelligenceCatalogItem](Set-CMAssetIntelligenceCatalogItem.md)


