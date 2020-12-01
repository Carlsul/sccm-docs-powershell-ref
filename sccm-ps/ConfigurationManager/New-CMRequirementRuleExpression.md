﻿---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMRequirementRuleExpression

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMRequirementRuleExpression [-AddAsGroup] [-AddExpression <ExpressionBase[]>]
 [-AddRequirementRule <Rule[]>] [-ClauseOperator <ConnectOperator>] [-GroupOperator <ConnectOperator>]
 [-RootExpression <ExpressionBase>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddAsGroup
{{ Fill AddAsGroup Description }}

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

### -AddExpression
{{ Fill AddExpression Description }}

```yaml
Type: ExpressionBase[]
Parameter Sets: (All)
Aliases: AddExpressions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequirementRule
{{ Fill AddRequirementRule Description }}

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases: AddRequirementRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClauseOperator
{{ Fill ClauseOperator Description }}

```yaml
Type: ConnectOperator
Parameter Sets: (All)
Aliases:
Accepted values: And, Or

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

### -GroupOperator
{{ Fill GroupOperator Description }}

```yaml
Type: ConnectOperator
Parameter Sets: (All)
Aliases:
Accepted values: And, Or

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootExpression
{{ Fill RootExpression Description }}

```yaml
Type: ExpressionBase
Parameter Sets: (All)
Aliases:

Required: False
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
