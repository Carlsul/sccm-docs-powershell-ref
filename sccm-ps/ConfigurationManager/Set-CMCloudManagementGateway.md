﻿---
description: Configure a cloud management gateway (CMG).
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Set-CMCloudManagementGateway
---

# Set-CMCloudManagementGateway

## SYNOPSIS

Configure a cloud management gateway (CMG).

## SYNTAX

### SetByValue (Default)
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -InputObject <IResultObject> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -Id <String> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -Name <String> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Configure a cloud management gateway (CMG).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the number of virtual machines for the CMG service

This example targets the CMG named **GraniteFalls** and changes the number of VMs to `4`.

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -VMInstancesCount 4
```

### Example 2: Update the CMG server authentication certificate

This example targets the CMG named **GraniteFalls** and updates the CMG server authentication certificate.

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -ServiceCertPath "c:\TestPath\NewServiceCert.pfx" -ServiceCertPassword (ConvertTo-SecureString -String "tX*xJ11Nuo^B" -AsPlainText -Force)
```

## PARAMETERS

### -CARootCert
{{ Fill CARootCert Description }}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: CARootCertificate, CARootCertificates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckClientCertRevocation

Set this parameter to `true` to verify client certificate revocation. A certificate revocation list (CRL) must be publicly published for this verification to work. For more information, see [Publish the certificate revocation list](https://docs.microsoft.com/mem/configmgr/core/clients/manage/cmg/security-and-privacy-for-cloud-management-gateway#bkmk_crl).

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

### -Description

Specify an optional description of this CMG service to better identify it.

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

### -EnableCloudDPFunction
{{ Fill EnableCloudDPFunction Description }}

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

### -EnableStorageQuota
{{ Fill EnableStorageQuota Description }}

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

### -EnableTrafficOut
{{ Fill EnableTrafficOut Description }}

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

### -EnforceProtocol
{{ Fill EnforceProtocol Description }}

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

### -Force

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

### -Id

Specify the Azure service ID of the CMG to configure.

```yaml
Type: String
Parameter Sets: SetById
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a CMG object to configure.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the CMG to configure.

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

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RemoveCertThumbprints
{{ Fill RemoveCertThumbprints Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertPassword

Applies to version 2006 and later. Specify the password for the certificate in the **-ServiceCertPath**.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: ServiceCertificatePassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertPath

Applies to version 2006 and later. Specify the path to the CMG server authentication certificate in PFX format. For more information, see [Certificates for CMG](https://docs.microsoft.com/mem/configmgr/core/clients/manage/cmg/certificates-for-cloud-management-gateway).

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceCertificatePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageCriticalPct
{{ Fill StorageCriticalPct Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageCriticalPercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaGB
{{ Fill StorageQuotaGB Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageWarningPct
{{ Fill StorageWarningPct Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageWarningPercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficCriticalPct

If you enable alerts for monitoring outbound data transfer, specify the percentage of threshold for raising a **Critical** alert. This value is `90` by default.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutGB

If you enable storage alerts, use this parameter to specify the storage alert threshold in **GB**. The default value is `2`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutStopService
{{ Fill TrafficOutStopService Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: StopTrafficOutService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficWarningPct

If you enable alerts for monitoring outbound data transfer, specify the percentage of threshold for raising a **Warning** alert. This value is `50` by default.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMInstanceCount
{{ Fill VMInstanceCount Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: VMInstancesCount

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

[Plan for the cloud management gateway](https://docs.microsoft.com/mem/configmgr/core/clients/manage/cmg/plan-cloud-management-gateway)
