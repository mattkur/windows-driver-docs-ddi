---
UID: NC:iddcx.EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN
title: EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN
author: windows-driver-content
description: EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN is called by the OS to inform the driver that a swapchain associated with a monitor is not valid anymore.
old-location: display\evt_idd_cx_monitor_unassign_swapchain.htm
old-project: display
ms.assetid: 7e845805-0121-49b0-9c0c-0f63bed6a50c
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.evt_idd_cx_monitor_unassign_swapchain, EvtIddCxMonitorUnassignSwapchain callback function [Display Devices], EvtIddCxMonitorUnassignSwapchain, EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN, EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN, iddcx/EvtIddCxMonitorUnassignSwapchain, PFN_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN callback function pointer [Display Devices], PFN_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: iddcx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: _requires_same_
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	UserDefined
apilocation: 
-	iddcx.h
apiname: 
-	PFN_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN
product: Windows
targetos: Windows
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
---

# EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN callback


## -description


<b>EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN</b> is called by the OS to inform the driver that a swapchain associated with a monitor is not valid anymore.


## -prototype


````
EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN EvtIddCxMonitorUnassignSwapchain;

NTSTATUS EvtIddCxMonitorUnassignSwapchain(
  _In_ IDDCX_MONITOR MonitorObject
)
{ ... }

typedef EVT_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN PFN_IDD_CX_MONITOR_UNASSIGN_SWAPCHAIN;
````


## -parameters




### -param MonitorObject [in]


                    
                A handle by the OS to identify the monitor that has an invalid associated swapchain.


## -returns



(NTSTATUS) If the operation is successful, the callback function must return STATUS_SUCCESS, or another status value for which NT_SUCCESS(status) equals TRUE. Otherwise, an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code. 
                    


