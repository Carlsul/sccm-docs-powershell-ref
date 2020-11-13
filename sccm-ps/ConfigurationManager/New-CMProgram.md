﻿---
description: Creates a new program in Configuration Manager.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMProgram
---

# New-CMProgram

## SYNOPSIS
Creates a new program in Configuration Manager.

## SYNTAX

### NewStandardProgram (Default)
```
New-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] -CommandLine <String>
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>] [-DriveLetter <String>]
 [-DriveMode <DriveModeType>] [-Duration <Int32>] -PackageName <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RunMode <RunModeType>] [-RunType <RunType>] -StandardProgramName <String>
 [-UserInteraction <Boolean>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewStandardProgramById
```
New-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] -CommandLine <String>
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>] [-DriveLetter <String>]
 [-DriveMode <DriveModeType>] [-Duration <Int32>] -PackageId <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RunMode <RunModeType>] [-RunType <RunType>] -StandardProgramName <String>
 [-UserInteraction <Boolean>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDeviceProgram
```
New-CMProgram -CommandLine <String> [-CommandLineFolder <String>] [-Comment <String>]
 -DeviceProgramName <String> [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageName <String> [-Requirement <String>]
 [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewDeviceProgramById
```
New-CMProgram -CommandLine <String> [-CommandLineFolder <String>] [-Comment <String>]
 -DeviceProgramName <String> [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageId <String> [-Requirement <String>]
 [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMProgram** cmdlet creates a program in Configuration Manager.
Programs are commands that are associated with a Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a standard program
```
PS XYZ:\> New-CMProgram -PackageName "test" -StandardProgramName SPM -CommandLine "RunMe" -WorkingDirectory "C:\temp" -RunType Hidden -ProgramRunType OnlyWhenNoUserIsLoggedOn -DiskSpaceRequirement 100 -DiskSpaceUnit GB -Duration 100 -DriveMode RenameWithUnc
```

This command creates a standard program in Configuration Manager.

### Example 2: Create a device program
```
PS XYZ:\> New-CMProgram -PackageName "Contoso-12" -DeviceProgramName DPM -Comment "Upgrades for December" -WorkingDirectory "C:\temp" -CommandLine "RunMe" -CommandLineFolder "C:\Windows\" -DiskSpaceRequirement 10 -DiskSpaceUnit GB -DownloadProgramType OnlyWhenTheDeviceIsDocked -Requirement "All previous updates"
```

This command creates a device program in Configuration Manager.

## PARAMETERS

### -AddSupportedOperatingSystemPlatform
```yaml
Type: IResultObject[]
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases: AddSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandLine
Specifies the command line for the program.

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

### -CommandLineFolder
Specifies the folder that contains the executable program.
This folder can be an absolute path on the client, or a path relative to the distribution folder that contains the package.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies optional text about a program, such as a description.
On client computers, this text is displayed in Run Advertised Programs in Control Panel.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceProgramName
Specifies a device program name.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
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

### -DiskSpaceRequirement
Specifies the amount of disk space that the software program requires to run on the computer.
If a value is specified, units for the value must also be specified.
The value must be greater than or equal to zero.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DiskSpaceReq

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSpaceUnit
Specifies the units for the *DiskSpaceRequirement* parameter.
The acceptable values for this parameter are: GB, KB, and MB.

```yaml
Type: DiskSpaceUnitType
Parameter Sets: (All)
Aliases:
Accepted values: KB, MB, GB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadProgramType
Specifies when the program is to run.
The acceptable values for this parameter are:

- AsSoonAsPossible
- OnlyOverFastNetwork
- OnlyWhenTheDeviceIsLocked.

```yaml
Type: DownloadProgramType
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:
Accepted values: AsSoonAsPossible, OnlyOverFastNetwork, OnlyWhenTheDeviceIsDocked

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveLetter
Specifies a drive letter to qualify the location if the *DriveMode* parameter is used.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveMode
Indicates whether the program requires a specific drive letter, specified in the *DriveLetter* parameter.
By default, the program runs with a Universal Naming Convention (UNC) name.
If *DriveMode* is set to RequiresDriveLetter, the program uses any available drive letter.
If *DriveMode* is set to RequiresSpecificDriveLetter, the program only runs if the drive is not already in use.

```yaml
Type: DriveModeType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: RunWithUnc, RequiresDriveLetter, RequiresSpecificDriveLetter

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Duration
Specifies the maximum amount of time the program is expected to run.
The default value is 120 minutes.

```yaml
Type: Int32
Parameter Sets: NewStandardProgram, NewStandardProgramById
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

### -PackageId
```yaml
Type: String
Parameter Sets: NewStandardProgramById, NewDeviceProgramById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies a package name.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewDeviceProgram
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramRunType
Specifies the logon conditions that are necessary for the program to run.
The acceptable values for this parameter are:

- OnlyWhenNoUserIsLoggedOn
- OnlyWhenUserIsLoggedOn
- WhetherOrNotUserIsLoggedOn

The default setting is OnlyWhenUserIsLoggedOn.

```yaml
Type: ProgramRunType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: OnlyWhenUserIsLoggedOn, WhetherOrNotUserIsLoggedOn, OnlyWhenNoUserIsLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reconnect
Indicates whether the client computer reconnects to the distribution point when the user logs on.

```yaml
Type: Boolean
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Requirement
Specifies additional requirements for standard or device programs.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases: Requirements

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunMode
Specifies the credentials that the program requires to run on the client computer.
The acceptable values for this parameter are: RunWithAdministrativeRights and RunWithUserRights.

```yaml
Type: RunModeType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: RunWithUserRights, RunWithAdministrativeRights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType
Specifies the mode is which the program will run on the client computer.
The acceptable values for this parameter are:

- Hidden
- Maximized
- Minimized
- Normal

The default is Normal.

```yaml
Type: RunType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: Normal, Minimized, Maximized, Hidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgramName
Specifies the standard program name.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserInteraction
Indicates whether to allow users to interact with the program.

```yaml
Type: Boolean
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkingDirectory
Specifies a working directory for the program.

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### None

## OUTPUTS

### IResultObject#SMS_Program

## NOTES

## RELATED LINKS

[Disable-CMProgram](Disable-CMProgram.md)

[Enable-CMProgram](Enable-CMProgram.md)

[Get-CMProgram](Get-CMProgram.md)

[Remove-CMProgram](Remove-CMProgram.md)

[Set-CMProgram](Set-CMProgram.md)


