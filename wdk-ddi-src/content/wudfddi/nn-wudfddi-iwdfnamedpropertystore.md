---
UID: NN:wudfddi.IWDFNamedPropertyStore
title: IWDFNamedPropertyStore
author: windows-driver-content
description: The IWDFNamedPropertyStore interface exposes a property-store object.
old-location: wdf\iwdfnamedpropertystore.htm
old-project: wdf
ms.assetid: f31a88c1-468f-4756-a5fa-b4aa0b8fe51d
ms.author: windowsdriverdev
ms.date: 1/11/2018
ms.keywords: wdf.iwdfnamedpropertystore, IWDFNamedPropertyStore interface, IWDFNamedPropertyStore interface, described, IWDFNamedPropertyStore, wudfddi/IWDFNamedPropertyStore, UMDFPropertyStoreObjectRef_139eb19f-8bb7-42ba-ab86-44f5f35e0faf.xml, umdf.iwdfnamedpropertystore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wudfddi.h
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
req.lib: wudfddi.h
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
-	IWDFNamedPropertyStore
product: Windows
targetos: Windows
req.typenames: *PPOWER_ACTION, POWER_ACTION
req.product: Windows 10 or later.
---

# IWDFNamedPropertyStore interface


## -description


<p class="CCE_Message">[<b>Warning:</b> UMDF 2 is the latest version of UMDF and supersedes UMDF 1.  All new UMDF drivers should be written using UMDF 2.  No new features are being added to UMDF 1 and there is limited support for UMDF 1 on newer versions of Windows 10.  Universal Windows drivers must use UMDF 2.  For more info, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/getting-started-with-umdf-version-2">Getting Started with UMDF</a>.]

The <b>IWDFNamedPropertyStore</b> interface exposes a property-store object.


## -members

The <b>IWDFNamedPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560182">IWDFNamedPropertyStore::GetNameAt</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f6ebf45b-b411-4684-b430-0b17a56ec0c0">GetNameAt</a> method retrieves the name of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560188">IWDFNamedPropertyStore::GetNameCount</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9891e360-ca09-4ebb-8cf4-d08b3456910c">GetNameCount</a> method retrieves the number of properties in a property store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560190">IWDFNamedPropertyStore::GetNamedValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9581e3af-f7f8-4365-8bb2-daedcb7a3280">GetNamedValue</a> method retrieves the value of a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff560195">IWDFNamedPropertyStore::SetNamedValue</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1fd075c9-7d0e-4670-bac0-b7b8ba0a714f">SetNamedValue</a> method sets the value of a property.

</td>
</tr>
</table>The <a href="https://msdn.microsoft.com/f6ebf45b-b411-4684-b430-0b17a56ec0c0">GetNameAt</a> method retrieves the name of a property.

The <a href="https://msdn.microsoft.com/9891e360-ca09-4ebb-8cf4-d08b3456910c">GetNameCount</a> method retrieves the number of properties in a property store.

The <a href="https://msdn.microsoft.com/9581e3af-f7f8-4365-8bb2-daedcb7a3280">GetNamedValue</a> method retrieves the value of a property.

The <a href="https://msdn.microsoft.com/1fd075c9-7d0e-4670-bac0-b7b8ba0a714f">SetNamedValue</a> method sets the value of a property.

 

