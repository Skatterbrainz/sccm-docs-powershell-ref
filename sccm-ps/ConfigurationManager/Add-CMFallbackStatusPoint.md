---
title: Add-CMFallbackStatusPoint
titleSuffix: Configuration Manager
description: Adds a fallback status point to a Configuration Manager site.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMFallbackStatusPoint

## SYNOPSIS
Adds a fallback status point to a Configuration Manager site.

## SYNTAX

### ByValue (Default)
```
Add-CMFallbackStatusPoint [-StateMessageNum <Int32>] [-ThrottleSec <Int32>] [-ThrottleMins <Int32>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMFallbackStatusPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-StateMessageNum <Int32>]
 [-ThrottleSec <Int32>] [-ThrottleMins <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMFallbackStatusPoint** cmdlet adds a fallback status point to a Microsoft System Center Configuration Manager site.
To add this site system role, specify the site code for the Configuration Manager site and the name of the computer that hosts the role.
You also need to specify a throttle interval and the number of messages for that throttle window.

Configuration Manager can use one or more fallback status points to collect state messages for a site and send them to Configuration Manager.
Throttling prevents the fallback status point from sending too many messages together, which can affect performance.
For more information, see [Install site system roles](https://docs.microsoft.com/sccm/core/servers/deploy/configure/install-site-system-roles).

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add a fallback status point
```
PS XYZ:\>Add-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "CMFSPPoint.Western.Contoso.com" -StateMessageNum 10000 -ThrottleInterval 60
```

This command adds a fallback status point for the site that has the site code CM1.
The specified computer hosts the role.
The command also specifies number of messages and throttle time period for the fallback status point.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessageNum
Specifies the number of state messages that a fallback status point can send to Configuration Manager within a throttle interval.

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

### -ThrottleMins
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

### -ThrottleSec
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThrottleIntervalSeconds, ThrottleInterval

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](Remove-CMFallbackStatusPoint.md)

[Set-CMFallbackStatusPoint](Set-CMFallbackStatusPoint.md)


