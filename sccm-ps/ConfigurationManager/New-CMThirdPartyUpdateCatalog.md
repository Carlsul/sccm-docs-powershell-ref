﻿---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# New-CMThirdPartyUpdateCatalog

## SYNOPSIS

Create a new third-party software updates catalog.

## SYNTAX

```
New-CMThirdPartyUpdateCatalog [-Description] <String> [-DownloadUrl] <Uri> [-Name] <String>
 [-PublisherName] <String> [[-SupportContact] <String>] [[-SupportUrl] <Uri>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a new third-party updates catalog. For more information, see [Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a third-party update catalog

```powershell
New-CMThirdPartyUpdateCatalog -DownloadUrl $downloadUrl -PublisherName $publisher -Name $name -Description $description -SupportUrl $supportUrl -SupportContact $supportContact
```

## PARAMETERS

### -Description

Specify a description for the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -DownloadUrl

Specify a valid HTTPS URL for the site to download the third-party update catalog.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### -Name

Specify a name for the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CatalogName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublisherName

Specify the publisher name of the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportContact

Specify the support contact for the third-party update catalog.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportUrl

Specify the support URL for the third-party update catalog.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_ISVCatalogs
## NOTES

This cmdlet returns the **SMS_ISVCatalogs** WMI class object.

## RELATED LINKS

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)
[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
