---
UID: NS:d3dkmthk._D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION
title: _D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION
author: windows-driver-content
description: The D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION structure describes the shared primary surface that an application is about to lock.
old-location: display\d3dkmt_sharedprimarylocknotification.htm
old-project: display
ms.assetid: 4e7766bb-eb5b-4f79-b9b8-89f7dcb98569
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION structure [Display Devices], d3dkmthk/D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION, D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION, _D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION, OpenGL_Structs_4ec11480-30cb-45a1-a31c-e7432ec45abf.xml, display.d3dkmt_sharedprimarylocknotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
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
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	d3dkmthk.h
apiname: 
-	D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION
product: Windows
targetos: Windows
req.typenames: D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION
---

# _D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION structure


## -description


The D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION structure describes the shared primary surface that an application is about to lock.


## -syntax


````
typedef struct _D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION {
  LUID                           AdapterLuid;
  D3DDDI_VIDEO_PRESENT_SOURCE_ID VidPnSourceId;
  RECTL                          LockRect;
} D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION;
````


## -struct-fields




### -field AdapterLuid

[in] The locally unique identifier (<a href="..\igpupvdev\ns-igpupvdev-_luid.md">LUID</a>) of the graphics adapter on which the GDI shared primary surface exists. 


### -field VidPnSourceId

[in] The zero-based identification number of the video present source in a path of a video present network (VidPN) topology on which the GDI shared primary surface exists. 


### -field LockRect

[in] A <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure that indicates the upper-left and lower-right points of a rectangle on the shared primary surface; the operating system disables all sprites that intersect with this rectangle. If the OpenGL ICD specifies zero for each member of RECTL, the operating system disables all sprites on the shared primary surface.


## -see-also

<a href="..\d3dkmthk\nf-d3dkmthk-d3dkmtsharedprimarylocknotification.md">D3DKMTSharedPrimaryLockNotification</a>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20D3DKMT_SHAREDPRIMARYLOCKNOTIFICATION structure%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

