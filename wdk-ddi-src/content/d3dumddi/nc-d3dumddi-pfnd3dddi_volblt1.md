---
UID: NC:d3dumddi.PFND3DDDI_VOLBLT1
title: PFND3DDDI_VOLBLT1
author: windows-driver-content
description: Performs a bit-block transfer (bitblt) operation from a source volume texture to a destination volume texture. Implemented by Windows Display Driver Model (WDDM) 1.2 or later user-mode display drivers.
old-location: display\volblt1.htm
old-project: display
ms.assetid: 81B9AB74-9CD1-4181-BE13-32D519069FD4
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.volblt1, VolBlt1 callback function [Display Devices], VolBlt1, PFND3DDDI_VOLBLT1, PFND3DDDI_VOLBLT1, d3dumddi/VolBlt1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3dumddi.h
req.include-header: D3dumddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	UserDefined
apilocation: 
-	d3dumddi.h
apiname: 
-	VolBlt1
product: Windows
targetos: Windows
req.typenames: DXGK_PTE
---

# PFND3DDDI_VOLBLT1 callback


## -description


Performs a bit-block transfer (bitblt) operation from a source volume texture to a destination volume texture. Implemented by Windows Display Driver Model (WDDM) 1.2 or later user-mode display drivers.


## -prototype


````
PFND3DDDI_VOLBLT1 VolBlt1;

__checkReturn HRESULT APIENTRY* VolBlt1(
  _In_       HANDLE               hDevice,
  _In_ const D3DDDIARG_VOLUMEBLT1 *pData
)
{ ... }
````


## -parameters




### -param hDevice [in]

 A handle to the display device (graphics context).


### -param *






#### - pData [in]

 A pointer to a <a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_volumeblt1.md">D3DDDIARG_VOLUMEBLT1</a> structure that defines the parameters for the volume bitblt operation.


## -returns



      Returns S_OK or an appropriate error result if the volume bitblt operation is not successfully performed.



## -see-also

<a href="..\d3dumddi\ns-d3dumddi-_d3dddiarg_volumeblt1.md">D3DDDIARG_VOLUMEBLT1</a>

<a href="..\d3dumddi\ns-d3dumddi-_d3dddi_devicefuncs.md">D3DDDI_DEVICEFUNCS</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3DDDI_VOLBLT1 callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

