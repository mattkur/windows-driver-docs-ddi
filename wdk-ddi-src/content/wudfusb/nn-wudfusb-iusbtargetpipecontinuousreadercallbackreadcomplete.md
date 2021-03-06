---
UID: NN:wudfusb.IUsbTargetPipeContinuousReaderCallbackReadComplete
title: IUsbTargetPipeContinuousReaderCallbackReadComplete
author: windows-driver-content
description: IUsbTargetPipeContinuousReaderCallbackReadComplete is a driver-supplied interface.
old-location: wdf\iusbtargetpipecontinuousreadercallbackreadcomplete.htm
old-project: wdf
ms.assetid: 953048ab-872c-4b94-8aef-bcfcb86ea4d8
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iusbtargetpipecontinuousreadercallbackreadcomplete, IUsbTargetPipeContinuousReaderCallbackReadComplete interface, IUsbTargetPipeContinuousReaderCallbackReadComplete interface, described, IUsbTargetPipeContinuousReaderCallbackReadComplete, wudfusb/IUsbTargetPipeContinuousReaderCallbackReadComplete, UMDFUSBref_bb387411-90fe-4347-910f-4c0fa535a309.xml, umdf.iusbtargetpipecontinuousreadercallbackreadcomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfusb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: wudfusb.h
req.dll: WUDFx.dll
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	wudfusb.h
apiname: 
-	IUsbTargetPipeContinuousReaderCallbackReadComplete
product: Windows
targetos: Windows
req.typenames: *PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE
req.product: Windows 10 or later.
---

# IUsbTargetPipeContinuousReaderCallbackReadComplete interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


<b>IUsbTargetPipeContinuousReaderCallbackReadComplete</b> is a driver-supplied interface.




## -members

The <b>IUsbTargetPipeContinuousReaderCallbackReadComplete</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556910">IUsbTargetPipeContinuousReaderCallbackReadComplete::OnReaderCompletion</a>
</td>
<td align="left" width="63%">
A driver's <a href="https://msdn.microsoft.com/946e0206-7609-4dc7-91c2-a6aadad91751">OnReaderCompletion</a> event callback function informs the driver that a continuous reader has successfully completed a read request.

</td>
</tr>
</table>A driver's <a href="https://msdn.microsoft.com/946e0206-7609-4dc7-91c2-a6aadad91751">OnReaderCompletion</a> event callback function informs the driver that a continuous reader has successfully completed a read request.

 

