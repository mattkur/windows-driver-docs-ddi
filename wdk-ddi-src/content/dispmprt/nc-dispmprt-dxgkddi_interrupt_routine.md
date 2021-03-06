---
UID: NC:dispmprt.DXGKDDI_INTERRUPT_ROUTINE
title: DXGKDDI_INTERRUPT_ROUTINE
author: windows-driver-content
description: The DxgkDdiInterruptRoutine function handles interrupts generated by a display adapter.
old-location: display\dxgkddiinterruptroutine.htm
old-project: display
ms.assetid: eacfd42d-405c-4c23-8978-0f373a393e10
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.dxgkddiinterruptroutine, DxgkDdiInterruptRoutine callback function [Display Devices], DxgkDdiInterruptRoutine, DXGKDDI_INTERRUPT_ROUTINE, DXGKDDI_INTERRUPT_ROUTINE, dispmprt/DxgkDdiInterruptRoutine, DmFunctions_5341cc5a-0dd5-4493-ab02-0aa66d910ec0.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: dispmprt.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
req.target-min-winversvr: 
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
req.irql: See Remarks section.
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	UserDefined
apilocation: 
-	dispmprt.h
apiname: 
-	DxgkDdiInterruptRoutine
product: Windows
targetos: Windows
req.typenames: SYMBOL_INFO_EX, *PSYMBOL_INFO_EX
---

# DXGKDDI_INTERRUPT_ROUTINE callback


## -description


The <i>DxgkDdiInterruptRoutine</i> function handles interrupts generated by a display adapter.


## -prototype


````
DXGKDDI_INTERRUPT_ROUTINE DxgkDdiInterruptRoutine;

BOOLEAN DxgkDdiInterruptRoutine(
  _In_ const PVOID MiniportDeviceContext,
  _In_       ULONG MessageNumber
)
{ ... }
````


## -parameters




### -param MiniportDeviceContext [in]

A handle to a context block associated with a display adapter. The display miniport driver's <a href="..\dispmprt\nc-dispmprt-dxgkddi_add_device.md">DxgkDdiAddDevice</a> function previously provided this handle to the DirectX graphics kernel subsystem.


### -param MessageNumber [in]

The message number if the interrupt is message-signaled. For line-based interrupts, this parameter is zero.


## -returns


If <i>DxgkDdiInterruptRoutine</i> determines that the adapter represented by <i>MiniportDeviceContext</i> did not generate the interrupt, it returns <b>FALSE</b>. Otherwise, it must dismiss the interrupt on the adapter before it returns <b>TRUE</b>.



## -remarks


If the interrupt is line-based (<i>MessageNumber</i> = 0), <i>DxgkDdiInterruptRoutine</i> must determine whether the adapter represented by <i>MiniportDeviceContext</i> generated the interrupt and, if not, return <b>FALSE</b> immediately.

If the adapter represented by <i>MiniportDeviceContext </i>did generate the interrupt, then <i>DxgkDdiInterruptRoutine</i> should perform the following steps:
<ul>
<li>
Dismiss the interrupt on the adapter.

</li>
<li>
Complete the requested operation that caused the interrupt, or queue a DPC that will complete the operation later. 

</li>
<li>
Return <b>TRUE</b> as quickly as possible.

</li>
</ul>Any other display miniport driver function that shares memory (for example, some portion of the state represented by <i>MiniportDeviceContext</i>) with <i>DxgkDdiInterruptRoutine</i> must call <a href="..\dispmprt\nc-dispmprt-dxgkcb_synchronize_execution.md">DxgkCbSynchronizeExecution</a> to synchronize its access to the shared memory.

The <i>DxgkDdiInterruptRoutine</i> function can call <a href="..\dispmprt\nc-dispmprt-dxgkcb_queue_dpc.md">DxgkCbQueueDpc</a> and <a href="..\d3dkmddi\nc-d3dkmddi-dxgkcb_notify_interrupt.md">DxgkCbNotifyInterrupt</a> but must not call any other <b>DxgkCbXxx</b> functions. For more information on the proper sequence of function calls, see <a href="https://msdn.microsoft.com/3622697a-3989-4756-89d4-c67c81815d49">Submitting a Command Buffer</a>.

<i>DxgkDdiInterruptRoutine</i> runs at an elevated IRQL, so it (and all the functions it calls) must be non-pageable. Also, <i>DxgkDdiInterruptRoutine</i> (and all the functions it calls) must not attempt to access pageable memory.



## -see-also

<a href="..\dispmprt\nc-dispmprt-dxgkcb_synchronize_execution.md">DxgkCbSynchronizeExecution</a>

<a href="..\dispmprt\nc-dispmprt-dxgkcb_queue_dpc.md">DxgkCbQueueDpc</a>

<a href="..\d3dkmddi\nc-d3dkmddi-dxgkcb_notify_interrupt.md">DxgkCbNotifyInterrupt</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20DXGKDDI_INTERRUPT_ROUTINE callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

