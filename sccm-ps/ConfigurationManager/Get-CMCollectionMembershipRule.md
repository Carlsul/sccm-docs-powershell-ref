﻿---
description: Get a Configuration Manager collection membership rule.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCollectionMembershipRule
---

# Get-CMCollectionMembershipRule

## SYNOPSIS
Get a Configuration Manager collection membership rule.

## SYNTAX

### ByName (Default)
```
Get-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> -CollectionName <String>
 [-CollectionType <CollectionType>] [-ExtraArguments <Object>] -RuleClassName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> -CollectionId <String>
 [-CollectionType <CollectionType>] [-ExtraArguments <Object>] -RuleClassName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionMembershipRule -ChildSearchCriteria <SmsProviderSearch> [-CollectionType <CollectionType>]
 [-ExtraArguments <Object>] -InputObject <IResultObject> -RuleClassName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is called by higher-level wrapper cmdlets. It isn't called directly.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

## PARAMETERS

### -ChildSearchCriteria
```yaml
Type: SmsProviderSearch
Parameter Sets: (All)
Aliases: SearchCriteria

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionType
```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Can't be combined with **ForceWildcardHandling**.

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

### -ExtraArguments
```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Can't be combined with **DisableWildcardHandling**.

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
```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleClassName
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.Object
### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
