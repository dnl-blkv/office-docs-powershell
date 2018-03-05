---
title: "Set-SPServiceApplicationPool"
ms.author: laurawi
author: LauraWi
manager: laurawi
ms.date: 3/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9daaee2-212c-4212-be07-225e7d88d83a

description: "Changes the account used for the Identity of the specified application pool."
---

# Set-SPServiceApplicationPool

Changes the account used for the Identity of the specified application pool.
  
```
Set-SPServiceApplicationPool [-Identity] <SPIisWebServiceApplicationPoolPipeBind> [[-Account] <SPProcessAccountPipeBind>] [-AssignmentCollection <SPAssignmentCollection>] [-Confirm [<SwitchParameter>]] [-WhatIf [<SwitchParameter>]]
```

## Detailed Description

The **Set-SPServiceApplicationPool** cmdlet changes the account used for the Identity of the specified application pool. 
  
For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [Windows PowerShell for SharePoint Server 2016 reference](https://go.microsoft.com/fwlink/p/?LinkId=671715).
  
## Parameters

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> |Specifies the identity of the Web service application pool to configure.  <br/> |
|**Account** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPProcessAccountPipeBind  <br/> |Specifies the credentials that will be the new Identity of the application pool.  <br/> |
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> |Manages objects for the purpose of proper disposal. Use of objects, such as **SPWeb** or **SPSite**, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the **SPAssignment** object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When **SPWeb**, **SPSite**, or **SPSiteAdministration** objects are used, the objects are automatically disposed of if an assignment collection or the **Global** parameter is not used.  <br/> > [!NOTE]> When the **Global** parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the **Stop-SPAssignment** command, an out-of-memory scenario can occur.           |
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Prompts you for confirmation before executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> |Displays a message that describes the effect of the command instead of executing the command. For more information, type the following command: **get-help about_commonparameters** <br/> |
   
## AutoGenParams

|**Parameter**|**Required**|**Type**|**Description**|
|:-----|:-----|:-----|:-----|
|**Identity** <br/> |Required  <br/> |Microsoft.SharePoint.PowerShell.SPIisWebServiceApplicationPoolPipeBind  <br/> ||
|**Account** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPProcessAccountPipeBind  <br/> ||
|**AssignmentCollection** <br/> |Optional  <br/> |Microsoft.SharePoint.PowerShell.SPAssignmentCollection  <br/> ||
|**Confirm** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
|**WhatIf** <br/> |Optional  <br/> |System.Management.Automation.SwitchParameter  <br/> ||
   
## Example

------------------EXAMPLE-----------------------
  
```
Set-SPServiceApplicationPool  TestServiceWebApplicationPool -Account testdomain\testuser1
```

This example changes the identity of the selected service application pool.
  
For the **Account** parameter, the name of a managed account in the farm can be given. Use the **Get-SPManagedAccount** cmdlet to view the existing managed account in the farm. Also, a process account from the output of the **Get-SPProcessAccount** cmdlet can be used. 
  
## See also

#### 

[Get-SPServiceApplicationPool](get-spserviceapplicationpool.md)
  
[New-SPServiceApplicationPool](new-spserviceapplicationpool.md)
  
[Remove-SPServiceApplicationPool](remove-spserviceapplicationpool.md)
