﻿---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMAdministrativeUserPermission

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByValue (Default)
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -InputObject <IResultObject> [-SecurityScope <IResultObject[]>]
 [-SecurityScopeId <String[]>] [-SecurityScopeName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -RoleId <String> [-SecurityScope <IResultObject[]>] [-SecurityScopeId <String[]>]
 [-SecurityScopeName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -RoleName <String> [-SecurityScope <IResultObject[]>]
 [-SecurityScopeId <String[]>] [-SecurityScopeName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Collection
{{ Fill Collection Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Collections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
{{ Fill CollectionId Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
{{ Fill CollectionName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionNames

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

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId
{{ Fill RoleId Description }}

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

### -RoleName
{{ Fill RoleName Description }}

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

### -SecurityScope
{{ Fill SecurityScope Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SecurityScopes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeId
{{ Fill SecurityScopeId Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName
{{ Fill SecurityScopeName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeNames

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

### IResultObject#SMS_APermission

## NOTES

## RELATED LINKS
