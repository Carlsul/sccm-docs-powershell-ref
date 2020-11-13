﻿---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Remove-CMDuplicateHardwareIdMacAddress

## SYNOPSIS

Use this cmdlet to remove duplicate hardware identifiers by MAC address.

## SYNTAX

### ByValue (Default)
```
Remove-CMDuplicateHardwareIdMacAddress -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMDuplicateHardwareIdMacAddress -MacAddress <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to remove duplicate hardware identifiers by MAC address.

## EXAMPLES

### Example 1: Specify an explicit MAC to remove

This example removes a hardware identifier for the specified MAC address.

```powershell
Remove-CMDuplicateHardwareIdMacAddress -MacAddress '01:02:03:04:05:E0'
```

### Example 2: Remove an ID for an input object

This example removes a hardware identifier for an input object `$myMacAddress`. This variable stores the identifier as `IResultObject#SMS_CommonMacAddresses`.

```powershell
Remove-CMDuplicateHardwareIdMacAddress -InputObject $myMacAddress
```

## PARAMETERS

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify an object for the hardware identifier to remove from the site. This object is of type `IResultObject#SMS_CommonMacAddresses`.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MacAddress

Specify a network MAC address of the hardware identifier to remove from the site. It's a colon-delimited (`:`) string value.

```yaml
Type: String
Parameter Sets: ByName
Aliases: DuplicateID, DuplicateHardwareId

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
Default value: None
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
Default value: None
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
