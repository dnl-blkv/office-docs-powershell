---
title: "Set-SPDiagnosticsProvider"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34911372-e971-4c40-bcab-880b45165886

description: "Enables a diagnostics provider and updates its retention policy."
---

# Set-SPDiagnosticsProvider

Enables a diagnostics provider and updates its retention policy.
  
```
Set-SPDiagnosticsProvider [-Identity] <SPDiagnosticsProviderPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-DaysRetained <Int32>] [-Enable <SwitchParameter>] [-MaxTotalSizeInBytes <Int64>] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPDiagnosticsProvider** cmdlet enables a diagnostics provider and updates its retention policy. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDiagnosticsProviderPipeBind  <br/> |Specifies the diagnostics provider to update.  <br/> The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a diagnostic provider (for example, DiagnosticProv1); or an instance of a valid **SPDiagnosticsProvider** object.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**DaysRetained** <br/> |Optional  <br/> |System.Int32  <br/> |Specifies the number of days to retain the data collected by a diagnostics provider.  <br/> The type must be a valid integer value in the range of **1** to **14**.  <br/> |
|**Enable** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Turns on or off the specified diagnostics provider.  <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPDiagnosticsProviderPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**DaysRetained** <br/> |Optional  <br/> |System.Int32  <br/> ||
|**Enable** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**MaxTotalSizeInBytes** <br/> |Optional  <br/> |System.Int64  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE 1-----------------------
  
```
Get-SPDiagnosticsProvider job-diagnostics-event-log-provider | Set-SPDiagnosticsProvider -Enable:$false
```

```
Get-SPDiagnosticsProvider job-diagnostics-event-log-provider
```

This example disables the event log diagnostics provider.
  
------------------EXAMPLE 2-----------------------
  
```
Get-SPDiagnosticsProvider job-diagnostics-event-log-provider | Set-SPDiagnosticsProvider -Enable -DaysRetained 10
```

```
Get-SPDiagnosticsProvider job-diagnostics-event-log-provider
```

This example enables the event log diagnostics provider and changes its retention policy to  `10` days. 
  
## See also

#### 

[Get-SPDiagnosticsProvider](get-spdiagnosticsprovider.md)
