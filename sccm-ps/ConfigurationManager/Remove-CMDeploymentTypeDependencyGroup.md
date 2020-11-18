---
description: Removes a deployment type dependency group from Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2018
schema: 2.0.0
title: Remove-CMDeploymentTypeDependencyGroup
---

# Remove-CMDeploymentTypeDependencyGroup

## SYNOPSIS

Removes a deployment type dependency group from Configuration Manager deployment type.

## SYNTAX

```
Remove-CMDeploymentTypeDependencyGroup [-Force] -InputObject <DeploymentTypeDependencyGroup>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMDeploymentTypeDependencyGroup** cmdlet removes a deployment type dependency group (and its dependencies) from a deployment type in the Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeDependencyGroup -GroupName MyGroup | Remove-CMDeploymentTypeDependencyGroup -Force
```

This command removes a deployment type dependency group.

## PARAMETERS

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

### -InputObject

Specifies a dependent type dependency group.

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

[New-CMDeploymentTypeDependencyGroup](./New-CMDeploymentTypeDependencyGroup.md)

[Get-CMDeploymentTypeDependencyGroup](./Get-CMDeploymentTypeDependencyGroup.md)

[Set-CMDeploymentTypeDependencyGroup](./Set-CMDeploymentTypeDependencyGroup.md)
