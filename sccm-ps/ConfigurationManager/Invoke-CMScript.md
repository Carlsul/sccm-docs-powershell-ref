﻿---
description: Invokes a script in Configuration Manager.
external help file: AdminUI.PS.ClientOperations.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/15/2018
schema: 2.0.0
title: Invoke-CMScript
---

# Invoke-CMScript

## SYNOPSIS

Invokes a script in Configuration Manager.

## SYNTAX

### ByInputObject
```
Invoke-CMScript [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-Device <IResultObject[]>] -InputObject <IResultObject> [-PassThru] [-ScriptParameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByGuid
```
Invoke-CMScript [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-Device <IResultObject[]>] [-PassThru] -ScriptGuid <String> [-ScriptParameter <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Invoke-CMScript** cmdlet invokes a PowerShell script in Configuration Manager. Configuration Manager has an integrated ability to run Powershell scripts. The scripts simplify building custom tools to administer software and let you accomplish mundane tasks quickly, allowing you to get large jobs done more easily and more consistently. For more information, see [Create and run PowerShell scripts from the Configuration Manager console](/sccm/apps/deploy-use/create-deploy-scripts).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Invoke a script by using the script id

```powershell
PS XYZ:\> Invoke-CMScript -ScriptGuid "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
```

This command invoke a script that has the ID DF8E7546-FD66-4A3D-A129-53AF5AA54F80  .

### Example 2: Invoke a script by using script object variable

```powershell
PS XYZ:\> $ScriptObj = Get-CMScript -Id "DF8E7546-FD66-4A3D-A129-53AF5AA54F80"
PS XYZ:\> Invoke-CMScript -InputObject $ScriptObj
```

The first command gets a **CMScript** object that has the ID DF8E7546-FD66-4A3D-A129-53AF5AA54F80, and then stores it in the $ScriptObj variable.

The second command invokes the script stored in the $ScriptObj variable.

## PARAMETERS

### -Collection

Specifies the collection.

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

### -CollectionId

Specifies the ID of a collection.

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

### -CollectionName

Specifies the name of a collection.

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

### -Device

Specifies a device object in Configuration Manager.
To obtain a device object, use the [Get-CMDevice](Get-CMDevice.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Devices

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

Specifies a **CMScript** object.
To obtain a **CMScript** object, use [Get-CMScript](Get-CMScript.md).

```yaml
Type: IResultObject
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -ScriptGuid

Specifies the script ID.

```yaml
Type: String
Parameter Sets: ByGuid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScriptParameter
{{ Fill ScriptParameter Description }}

```yaml
Type: Hashtable
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Approve-CMScript](Approve-CMScript.md)

[Deny-CMScript](Deny-CMScript.md)

[Get-CMScript](Invoke-CMScript.md)

[Remove-CMScript](Remove-CMScript.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Add-CMScriptDeploymentType](Add-CMScriptDeploymentType.md)
