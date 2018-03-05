---
title: "Restart-SPAppInstanceJob"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 064b972d-ca75-4de6-b863-5510e5bce9aa

description: "Restarts an app instance."
---

# Restart-SPAppInstanceJob

Restarts an app instance.
  
```
Restart-SPAppInstanceJob -AppInstance <SPAppInstance> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

Use the **Restart-SPAppInstanceJob** cmdlet to restart an app instance. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppInstance** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> |Specifies the app instance object to restart.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**AppInstance** <br/> |Required  <br/> |Microsoft.SharePoint.Administration.SPAppInstance  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

-----------EXAMPLE-------------
  
```
$instance = Get-SPAppInstance -AppInstanceId $instance.Id
```

```
Restart-SPAppInstanceJob -AppInstance $instance
```

This example restarts an instance of an app by first returning the ID of the instance and then restarting it.
  
## See also

#### 

[Get-SPAppInstance](get-spappinstance.md)
  
[Uninstall-SPAppInstance](uninstall-spappinstance.md)
  
[Uninstall-SPAppInstance](uninstall-spappinstance.md)
