---
UID: NS:usbsidebandaudio._USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS
title: _USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS
author: windows-driver-content
description: TBD.
old-location: audio\usbsidebandaudio_stream_status_params.htm
old-project: audio
ms.assetid: 5C50D9B0-53C7-4F1B-A6D1-CE77A3645956
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, usbsidebandaudio/PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS structure [Audio Devices], usbsidebandaudio/USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, *PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS structure pointer [Audio Devices], audio.usbsidebandaudio_stream_status_params, _USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: usbsidebandaudio.h
req.include-header: Usbsidebandaudio.h
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
req.lib: 
req.dll: 
req.irql: 
topictype: 
-	kbSyntax
apitype: 
-	<TBD>
apilocation: 
-	
apiname: 
-	USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS
product: Windows
targetos: Windows
req.typenames: *PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS
req.product: Windows 10 or later.
---

# _USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

TBD


## -syntax


````
typedef struct _USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS {
  ULONG    Reserved 0;
  BOOL     Reserved 1;
  NTSTATUS Reserved 2;
} USBSIDEBANDAUDIO_STREAM_STATUS_PARAMS, *PUSBSIDEBANDAUDIO_STREAM_STATUS_PARAMS;
````


## -struct-fields




### -field EpIndex

 


### -field Immediate

 


### -field Status

 



#### - Reserved 1

TBD


#### - Reserved 0

TBD


#### - Reserved 2

TBD

