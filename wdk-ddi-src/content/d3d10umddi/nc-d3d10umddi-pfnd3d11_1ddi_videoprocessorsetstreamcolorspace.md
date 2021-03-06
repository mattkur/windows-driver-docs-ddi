---
UID: NC:d3d10umddi.PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE
title: PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE
author: windows-driver-content
description: Sets the color space for an input stream on the video processor.
old-location: display\videoprocessorsetstreamcolorspace.htm
old-project: display
ms.assetid: bb187968-ae2a-4872-a745-fb42c0cff528
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.videoprocessorsetstreamcolorspace, pfnVideoProcessorSetStreamColorSpace callback function [Display Devices], pfnVideoProcessorSetStreamColorSpace, PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE, PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE, d3d10umddi/pfnVideoProcessorSetStreamColorSpace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
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
-	D3d10umddi.h
apiname: 
-	pfnVideoProcessorSetStreamColorSpace
product: Windows
targetos: Windows
req.typenames: *PSETRESULT_INFO, SETRESULT_INFO
---

# PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE callback


## -description


Sets the color space for an input stream on the video processor.






## -prototype


````
PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE pfnVideoProcessorSetStreamColorSpace;

VOID APIENTRY* pfnVideoProcessorSetStreamColorSpace(
  _In_       D3D10DDI_HDEVICE                       hDevice,
  _In_       D3D11_1DDI_HVIDEOPROCESSOR             hVideoProcessor,
  _In_       UINT                                   StreamIndex,
  _In_ const D3D11_1DDI_VIDEO_PROCESSOR_COLOR_SPACE *pColorSpace
)
{ ... }
````


## -parameters




### -param D3D10DDI_HDEVICE



### -param D3D11_1DDI_HVIDEOPROCESSOR



### -param UINT



### -param *






#### - StreamIndex [in]

The zero-based index of the input stream.


#### - hVideoProcessor [in]

A handle to the video processor object that was created through a call to the <a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessor.md">CreateVideoProcessor</a> function. 




#### - hDevice [in]

A handle to the display device (graphics context).




#### - pColorSpace [in]

A pointer to a <a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_color_space.md">D3D11_1DDI_VIDEO_PROCESSOR_COLOR_SPACE</a> structure that specifies the color space for the specified input stream.


## -returns


This callback function does not return a value.



## -see-also

<a href="..\d3d10umddi\nc-d3d10umddi-pfnd3d11_1ddi_createvideoprocessor.md">CreateVideoProcessor</a>

<a href="..\d3d10umddi\ns-d3d10umddi-d3d11_1ddi_video_processor_color_space.md">D3D11_1DDI_VIDEO_PROCESSOR_COLOR_SPACE</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [display\display]:%20PFND3D11_1DDI_VIDEOPROCESSORSETSTREAMCOLORSPACE callback function%20 RELEASE:%20(12/29/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

