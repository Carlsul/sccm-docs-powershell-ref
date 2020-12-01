﻿---
description: Creates a new Active Directory Query type global condition in Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/07/2019
schema: 2.0.0
title: New-CMGlobalConditionActiveDirectoryQuery
---

# New-CMGlobalConditionActiveDirectoryQuery

## SYNOPSIS

Creates a new Active Directory Query type global condition in Configuration Manager.

## SYNTAX

```
New-CMGlobalConditionActiveDirectoryQuery -DataType <GlobalConditionDataType> -DistinguishedName <String>
 -LdapFilter <String> [-LdapPrefix <String>] -Property <String> -SearchScope <SearchScope>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMGlobalConditionActiveDirectoryQuery** cmdlet creates a Active Directory Query type global condition in Configuration Manager.

A global condition is a setting or expression in Configuration Manager that you can use to specify how Configuration Manager provides and deploys an application to clients.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
$GlobalQuery = New-CMGlobalConditionActiveDirectoryQuery -Name GC1 -DataType String -DistinguishedName "CN=Users" -LdapPrefix "LDAP://" -LdapFilter "DC=Vlan123DOM" -Property "DC=net" -SearchScope Base -Description $String
```

This command creates a new Active Directory Query type global condition in Configuration Manager.

## PARAMETERS

### -DataType

Specifies a global condition data type.

```yaml
Type: GlobalConditionDataType
Parameter Sets: (All)
Aliases:
Accepted values: String, DateTime, Integer, FloatingPoint, Version, Boolean, StringArray, IntegerArray

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description.

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

### -DistinguishedName

Specifies a distinguished name.

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

### -LdapFilter

Specifies a LDAP filter to refine the results from the Active Directory Domain Services query to assess compliance on client computers.

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

### -LdapPrefix

Specifies a valid LDAP prefix to the Active Directory Domain Services query to assess compliance on client computers. You can use either LDAP:// or GC://.

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

### -Name

Specifies a name for the Active Directory Query global condition.

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

### -Property

Specifies the property of the Active Directory Domain Services object that will be used to assess compliance on client computers.

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

### -SearchScope

Specifies the search scope in Active Directory Domain Services:

- **Base** - Queries only the specified object.
- **One Level** - This option is not used in this version of Configuration Manager.
- **Subtree** - Queries the specified object and its complete subtree in the directory.

```yaml
Type: SearchScope
Parameter Sets: (All)
Aliases:
Accepted values: Base, OneLevel, Subtree

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Set-CMGlobalConditionActiveDirectoryQuery](./Set-CMGlobalConditionActiveDirectoryQuery.md)

[New-CMGlobalCondition](./New-CMGlobalCondition.md)

[New-CMGlobalConditionAssembly](./New-CMGlobalConditionAssembly.md)

[New-CMGlobalConditionFile](./New-CMGlobalConditionFile.md)

[New-CMGlobalConditionIisMetabase](./New-CMGlobalConditionIisMetabase.md)

[New-CMGlobalConditionOmaUri](./New-CMGlobalConditionOmaUri.md)

[New-CMGlobalConditionRegistryKey](./New-CMGlobalConditionRegistryKey.md)

[New-CMGlobalConditionRegistryValue](./New-CMGlobalConditionRegistryValue.md)

[New-CMGlobalConditionScript](./New-CMGlobalConditionScript.md)

[New-CMGlobalConditionSqlQuery](./New-CMGlobalConditionSqlQuery.md)

[New-CMGlobalConditionWqlQuery](./New-CMGlobalConditionWqlQuery.md)

[New-CMGlobalConditionXPathQuery](./New-CMGlobalConditionXpathQuery.md)
