---
description: Sets a Configuration Manager collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMCollection
---

# Set-CMCollection

## SYNOPSIS
Sets a Configuration Manager collection.

## SYNTAX

### SetByValue (Default)
```
Set-CMCollection [-Comment <String>] -InputObject <IResultObject> [-LimitingCollection <IResultObject>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMCollection -CollectionId <String> [-Comment <String>] [-LimitingCollection <IResultObject>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCollection [-Comment <String>] [-LimitingCollection <IResultObject>] [-LimitingCollectionId <String>]
 [-LimitingCollectionName <String>] -Name <String> [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
**The Set-CMCollection** cmdlet changes settings for a collection in Configuration Manager.

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a collection and modify it
```
PS XYZ:\> $userCollection = Get-CMCollection -Name "testUser"
PS XYZ:\> Set-CMCollection -CollectionId $userCollection -NewName "newTestUser"
```

The first command gets the collection object named testUser and stores the object in the $userCollection variable.

The second command updates the name of the collection in $userCollection.

### Example 2: Pass a collection and modify it
```
PS XYZ:\> Get-CMCollection -Name "testUser" | Set-CMCollection -NewName "newTestUser"
```

This command gets the collection object named testUser and uses the pipeline operator to pass the object to **Set-CMCollection**, which updates its name to newTestUser.

## PARAMETERS

### -CollectionId
Specifies a collection ID.

```yaml
Type: String
Parameter Sets: SetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a comment for the collection.

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

### -InputObject
Specifies a collection object.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollection
Specifies a collection object to use as a scope for this collection.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -LimitingCollectionId
Specifies the ID of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LimitToCollectionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName
Specifies the name of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LimitToCollectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the collection.

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

### -RefreshSchedule
Specifies a schedule that determines when Configuration Manager refreshes the collection.

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

### -RefreshType
Specifies how Configuration Manager refreshes the collection.
Valid values are:

- None
- Manual
- Periodic
- Continuous
- Both

```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases:
Accepted values: None, Manual, Periodic, Continuous, Both

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariablePriority
{{ Fill VariablePriority Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DeviceCollectionVariablePrecedence

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

[Get-CMCollection](Get-CMCollection.md)

[Export-CMCollection](Export-CMCollection.md)

[Import-CMCollection](Import-CMCollection.md)

[New-CMCollection](New-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)
