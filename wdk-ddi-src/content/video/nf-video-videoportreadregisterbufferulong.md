---
UID: NF:video.VideoPortReadRegisterBufferUlong
title: VideoPortReadRegisterBufferUlong function
author: windows-driver-content
description: The VideoPortReadRegisterBufferUlong function reads a number of ULONG values from a mapped device memory range and writes them into a buffer.
old-location: display\videoportreadregisterbufferulong.htm
old-project: display
ms.assetid: ebef1d9f-9559-436c-b425-92ccf3bbf203
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: VideoPortReadRegisterBufferUlong function [Display Devices], video/VideoPortReadRegisterBufferUlong, display.videoportreadregisterbufferulong, VideoPortReadRegisterBufferUlong, VideoPort_Functions_69ff5729-b386-4527-8bca-adc70e2d467d.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: video.h
req.include-header: Video.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Videoprt.lib
req.dll: Videoprt.sys
req.irql: See Remarks section.
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	DllExport
apilocation: 
-	Videoprt.sys
apiname: 
-	VideoPortReadRegisterBufferUlong
product: Windows
targetos: Windows
req.typenames: VIDEO_PORT_SERVICES
req.product: Windows 10 or later.
---

# VideoPortReadRegisterBufferUlong function


## -description


The <b>VideoPortReadRegisterBufferUlong</b> function reads a number of ULONG values from a mapped device memory range and writes them into a buffer.


## -syntax


````
VOID VideoPortReadRegisterBufferUlong(
        PULONG Register,
  _Out_ PULONG Buffer,
        ULONG  Count
);
````


## -parameters




### -param Register

Pointer to the register. The given <i>Register</i> must be in a mapped memory-space range returned by <a href="..\video\nf-video-videoportgetdevicebase.md">VideoPortGetDeviceBase</a>.


### -param Buffer [out]

Pointer to a buffer into which the ULONG values are written.


### -param Count

Specifies the number of ULONG values to be written to the buffer.


## -returns


None



## -remarks


The buffer must be large enough to contain at least the specified number of ULONG values.

A miniport driver's <a href="..\video\nc-video-pvideo_hw_interrupt.md">HwVidInterrupt</a> or <a href="..\video\nc-video-pminiport_synchronize_routine.md">HwVidSynchronizeExecutionCallback</a> function can call <b>VideoPortReadRegisterBufferUlong</b>.

Callers of <b>VideoPortReadRegisterBufferUlong</b> can be running at any IRQL, provided that the memory pointed to by the <i>Buffer</i> parameter is resident and that pointed to by the <i>Register</i> parameter is resident, mapped device memory.



## -see-also

<a href="..\video\nf-video-videoportgetdevicebase.md">VideoPortGetDeviceBase</a>

<a href="..\video\nc-video-pvideo_hw_interrupt.md">HwVidInterrupt</a>

<a href="..\video\nc-video-pminiport_synchronize_routine.md">HwVidSynchronizeExecutionCallback</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20VideoPortReadRegisterBufferUlong function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

