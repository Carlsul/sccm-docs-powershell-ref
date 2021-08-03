---
description: Adds a reporting service point to Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMReportingServicePoint
---

# Add-CMReportingServicePoint

## SYNOPSIS
Adds a reporting service point to Configuration Manager.

## SYNTAX

### ReportingServicePointByValue (Default)
```
Add-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-Force]
 -InputObject <IResultObject> [-ReportServerInstance <String>] -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ReportingServicePoint
```
Add-CMReportingServicePoint [-DatabaseName <String>] [-DatabaseServerName <String>] [-FolderName <String>]
 [-Force] [-ReportServerInstance <String>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 -UserName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMReportingServicePoint** cmdlet adds a reporting service point to Configuration Manager.
A reporting service point is a site system role that is installed on a server that run Microsoft SQL Server Reporting Services.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a reporting service point
```
PS XYZ:\>Add-CMReportingServicePoint -SiteCode "CM1" -SiteSystemServerName "CMReportingServicePoint.TSQA.Contoso.com"
```

This command adds a reporting service point on the computer named CMReportingServicePoint.TSQA.Contoso.com for the Configuration Manager site that has the site code CM1.

## PARAMETERS

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

### -DatabaseName
Specifies the name of the Configuration Manager database that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.

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

### -DatabaseServerName
Specifies the name of the Configuration Manager database server that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.
To specify a database instance, use the format \<Server Name\>\\\<Instance Name\>.

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

### -FolderName
Specifies the name of the report folder on the report server.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Run the command without asking for confirmation.

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ReportingServicePointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReportServerInstance
Specifies the name of an instance of Microsoft SQL Server Reporting Services.

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

### -SiteCode
Specifies a site code of a Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies a user name for an account that Configuration Manager uses to connect with Microsoft SQL Server Reporting Services and that gives this user access to the site database.

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

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Get-CMReportingServicePoint](Get-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](Remove-CMReportingServicePoint.md)

[Set-CMReportingServicePoint](Set-CMReportingServicePoint.md)


