﻿---
description: Adds a deployment type as a dependency to a dependency group in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/02/2019
schema: 2.0.0
title: Add-CMDeploymentTypeDependency
---

# Add-CMDeploymentTypeDependency

## SYNOPSIS

Adds a deployment type as a dependency to a dependency group in Configuration Manager.

## SYNTAX

```
Add-CMDeploymentTypeDependency -DeploymentTypeDependency <IResultObject[]>
 -InputObject <DeploymentTypeDependencyGroup> [-IsAutoInstall <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Add-CMDeploymentTypeDependency** adds a deployment type as a dependency to a dependency group. Required input is a deployment type object from [Get-CMDeploymentType](./Get-CMDeploymentType.md) and a dependency group from [Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md) and [New-CMDeploymentTypeDependencyGroup](./New-CMDeploymentTypeDependencyGroup.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | New-CMDeploymentTypeDependencyGroup -GroupName MyGroup | Add-CMDeploymentTypeDependency -DeploymentTypeDependency (Get-CMDeploymentType -ApplicationName MyChildApp) -IsAutoInstall $true
```

This command adds a deployment type dependency.

## PARAMETERS

### -DeploymentTypeDependency

Specifies a deployment type object.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
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

Specifies a deployment type dependency group object.

```yaml
Type: DeploymentTypeDependencyGroup
Parameter Sets: (All)
Aliases: Group

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsAutoInstall

Indicate whether install automatically.

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

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### Microsoft.ConfigurationManagement.Cmdlets.AppMan.Commands.DeploymentTypeDependencyGroup

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMDeploymentTypeDependency](./Get-CMDeploymentTypeDependency.md)

[Set-CMDeploymentTypeDependency](./Set-CMDeploymentTypeDependency.md)

[Remove-CMDeploymentTypeDependency](./Remove-CMDeploymentTypeDependency.md)
