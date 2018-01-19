---
UID: NF:wudfusb.IWDFUsbRequestCompletionParams.GetPipeWriteParameters
title: IWDFUsbRequestCompletionParams::GetPipeWriteParameters method
author: windows-driver-content
description: The GetPipeWriteParameters method retrieves parameters that are associated with the completion of a write request.
old-location: wdf\iwdfusbrequestcompletionparams_getpipewriteparameters.htm
old-project: wdf
ms.assetid: c6824215-0c16-471e-aea9-1b5cbeb2286b
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: IWDFUsbRequestCompletionParams, IWDFUsbRequestCompletionParams::GetPipeWriteParameters, GetPipeWriteParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wudfusb.h
req.include-header: Wudfusb.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 1.5
req.alt-api: IWDFUsbRequestCompletionParams.GetPipeWriteParameters
req.alt-loc: WUDFx.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: Unavailable in UMDF 2.0 and later.
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: WUDFx.dll
req.irql: 
req.typenames: *PWDF_USB_REQUEST_TYPE, WDF_USB_REQUEST_TYPE
req.product: Windows 10 or later.
---

# IWDFUsbRequestCompletionParams::GetPipeWriteParameters method



## -description
<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>GetPipeWriteParameters</b> method retrieves parameters that are associated with the completion of a write request.



## -syntax

````
void GetPipeWriteParameters(
  [out, optional] IWDFMemory **ppWriteMemory,
  [out, optional] SIZE_T     *pBytesWritten,
  [out, optional] SIZE_T     *pWriteMemoryOffset
);
````


## -parameters

### -param ppWriteMemory [out, optional]

A pointer to a variable that receives a pointer to the <a href="..\wudfddi\nn-wudfddi-iwdfmemory.md">IWDFMemory</a> interface, for access to the write buffer for the write request. This parameter is optional and can be <b>NULL</b>.


### -param pBytesWritten [out, optional]

A pointer to a variable that receives the size, in bytes, of the write buffer for the write request. This parameter is optional and can be <b>NULL</b>.


### -param pWriteMemoryOffset [out, optional]

A pointer to a variable that receives the offset, in bytes, into the write buffer for the write request. This parameter is optional and can be <b>NULL</b>.


## -returns
None


## -remarks


## -see-also
<dl>
<dt>
<a href="..\wudfusb\nn-wudfusb-iwdfusbrequestcompletionparams.md">IWDFUsbRequestCompletionParams</a>
</dt>
<dt>
<a href="..\wudfddi\nn-wudfddi-iwdfmemory.md">IWDFMemory</a>
</dt>
</dl>
 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [wdf\wdf]:%20IWDFUsbRequestCompletionParams::GetPipeWriteParameters method%20 RELEASE:%20(1/11/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>
