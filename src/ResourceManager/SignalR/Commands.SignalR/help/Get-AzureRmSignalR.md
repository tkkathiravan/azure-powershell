---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/get-azurermsignalrkey
schema: 2.0.0
---

# Get-AzureRmSignalR

## SYNOPSIS
Get a specific SignalR service or all the SignalR services in a resource group or a subscription.

## SYNTAX

### ListSignalRServiceParameterSet (Default)
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupParameterSet
```
Get-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmSignalR -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
Get a specific SignalR service or all the SignalR services in a resource group or a subscription.

## EXAMPLES

### Get all SignalR services in the subscription
```powershell
PS C:\> Get-AzureRmSignalR

HostName                                           Location       ServerPort PublicPort ProvisioningState
--------                                           --------       ---------- ---------- -----------------
mysignalr1.servicedev.signalr.net                  eastus         5002       5001       Succeeded
mysignalr2.servicedev.signalr.net                  eastus         5002       5001       Succeeded
mysignalr3.servicedev.signalr.net                  eastus         5002       5001       Creating
```

### Get all SignalR services in a resource group

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup

HostName                                           Location       ServerPort PublicPort ProvisioningState
--------                                           --------       ---------- ---------- -----------------
mysignalr1.servicedev.signalr.net                  eastus         5002       5001       Succeeded
mysignalr2.servicedev.signalr.net                  eastus         5002       5001       Succeeded
```

### Get a specific SignalR service

```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1

HostName                                           Location       ServerPort PublicPort ProvisioningState
--------                                           --------       ---------- ---------- -----------------
mysignalr1.servicedev.signalr.net                  eastus         5002       5001       Succeeded
```

### Get a specific SignalR service from the default resource group

```powershell
PS C:\> Get-AzureRmSignalR -Name mysignalr2

HostName                                           Location       ServerPort PublicPort ProvisioningState
--------                                           --------       ---------- ---------- -----------------
mysignalr2.servicedev.signalr.net                  eastus         5002       5001       Succeeded
```

The default resource group can be set by `Set-AzureRmDefault -ResourceGroupName myResourceGroup`.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
SignalR service name.

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resource group name.

```yaml
Type: String
Parameter Sets: ListSignalRServiceParameterSet, ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
The SignalR service resource ID.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource

## NOTES

## RELATED LINKS