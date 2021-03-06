---
UID: NN:wudfusb.IWDFUsbTargetPipe
title: IWDFUsbTargetPipe
author: windows-driver-content
description: The IWDFUsbTargetPipe interface exposes a USB pipe (endpoint), which is also an I/O target.
old-location: wdf\iwdfusbtargetpipe.htm
old-project: wdf
ms.assetid: 16364b13-d902-4ba3-8d0a-c044946afa1e
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iwdfusbtargetpipe, IWDFUsbTargetPipe interface, IWDFUsbTargetPipe interface, described, IWDFUsbTargetPipe, wudfusb/IWDFUsbTargetPipe, UMDFUSBref_985f9453-7475-4e9b-894c-5d4e7b8d3971.xml, umdf.iwdfusbtargetpipe
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfusb.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
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
-	WUDFx.dll
apiname: 
-	IWDFUsbTargetPipe
product: Windows
targetos: Windows
req.typenames: *PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE
req.product: Windows 10 or later.
---

# IWDFUsbTargetPipe interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]


The <b>IWDFUsbTargetPipe</b> interface exposes a USB pipe (endpoint), which is also an I/O target.




## -members

The <b>IWDFUsbTargetPipe</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560397">IWDFUsbTargetPipe::Abort</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f756988d-8b21-4c2e-8c85-68f4eaa2c4f9">Abort</a> method aborts all pending transfers on a USB pipe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560400">IWDFUsbTargetPipe::Flush</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a> method discards any data that WinUsb saved when the device returned more data than the client requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560403">IWDFUsbTargetPipe::GetInformation</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b1462a64-debf-441f-8964-4644074e5e53">GetInformation</a> method retrieves information about a USB pipe (endpoint).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560406">IWDFUsbTargetPipe::GetType</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a> method retrieves the type of a USB pipe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560410">IWDFUsbTargetPipe::IsInEndPoint</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c1cba1fa-3952-4f2f-829f-2f5983349df8">IsInEndPoint</a> method determines whether a USB pipe (endpoint) is an IN pipe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560414">IWDFUsbTargetPipe::IsOutEndPoint</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/cb6c5b25-ea21-44cb-8b67-c5266c8bc1e4">IsOutEndPoint</a> method determines whether a USB pipe (endpoint) is an OUT pipe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560416">IWDFUsbTargetPipe::Reset</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method resets the data toggle and clears the stall condition on a USB pipe.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560418">IWDFUsbTargetPipe::RetrievePipePolicy</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/578f7633-307e-4cda-b8fe-ae73a095976f">RetrievePipePolicy</a> method retrieves a WinUsb pipe policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560421">IWDFUsbTargetPipe::SetPipePolicy</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3c8f5c4a-a1a3-41a9-ae55-f83048aab0ec">SetPipePolicy</a> method sets the WinUsb pipe policy.

</td>
</tr>
</table>The <a href="https://msdn.microsoft.com/f756988d-8b21-4c2e-8c85-68f4eaa2c4f9">Abort</a> method aborts all pending transfers on a USB pipe.

The <a href="https://msdn.microsoft.com/library/windows/hardware/hh463886">Flush</a> method discards any data that WinUsb saved when the device returned more data than the client requested.

The <a href="https://msdn.microsoft.com/b1462a64-debf-441f-8964-4644074e5e53">GetInformation</a> method retrieves information about a USB pipe (endpoint).

The <a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a> method retrieves the type of a USB pipe.

The <a href="https://msdn.microsoft.com/c1cba1fa-3952-4f2f-829f-2f5983349df8">IsInEndPoint</a> method determines whether a USB pipe (endpoint) is an IN pipe.

The <a href="https://msdn.microsoft.com/cb6c5b25-ea21-44cb-8b67-c5266c8bc1e4">IsOutEndPoint</a> method determines whether a USB pipe (endpoint) is an OUT pipe.

The <a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method resets the data toggle and clears the stall condition on a USB pipe.

The <a href="https://msdn.microsoft.com/578f7633-307e-4cda-b8fe-ae73a095976f">RetrievePipePolicy</a> method retrieves a WinUsb pipe policy.

The <a href="https://msdn.microsoft.com/3c8f5c4a-a1a3-41a9-ae55-f83048aab0ec">SetPipePolicy</a> method sets the WinUsb pipe policy.

 

