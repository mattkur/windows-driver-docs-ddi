---
UID: NE:d3dkmthk._D3DKMT_BRIGHTNESS_INFO_TYPE
title: _D3DKMT_BRIGHTNESS_INFO_TYPE
author: windows-driver-content
description: Indicates the type of information to retrieve or set for the brightness of an integrated display panel.
old-location: display\d3dkmt_brightness_info_type.htm
old-project: display
ms.assetid: 0f37ac57-9f3b-4bbc-a927-ea85aa44f910
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: D3DKMT_BRIGHTNESS_INFO_SET_OPTIMIZATION, D3DKMT_BRIGHTNESS_INFO_GET_POSSIBLE_LEVELS, D3DKMT_BRIGHTNESS_INFO_GET_REDUCTION, display.d3dkmt_brightness_info_type, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_GET_REDUCTION, D3DKMT_BRIGHTNESS_INFO_SET_STATE, D3DKMT_BRIGHTNESS_INFO_GET, D3DKMT_BRIGHTNESS_INFO_GET_CAPS, D3DKMT_BRIGHTNESS_INFO_TYPE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_TYPE, D3DKMT_BRIGHTNESS_INFO_BEGIN_MANUAL_MODE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_TOGGLE_LOGGING, D3DKMT_BRIGHTNESS_INFO_END_MANUAL_MODE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_SET_STATE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_SET, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_GET_CAPS, D3DKMT_BRIGHTNESS_INFO_SET, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_BEGIN_MANUAL_MODE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_GET_POSSIBLE_LEVELS, D3DKMT_BRIGHTNESS_INFO_TOGGLE_LOGGING, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_SET_OPTIMIZATION, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_END_MANUAL_MODE, D3DKMT_BRIGHTNESS_INFO_TYPE enumeration [Display Devices], _D3DKMT_BRIGHTNESS_INFO_TYPE, d3dkmthk/D3DKMT_BRIGHTNESS_INFO_GET
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3dkmthk.h
req.include-header: D3dkmthk.h
req.target-type: Windows
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
-	HeaderDef
apilocation: 
-	D3dkmthk.h
apiname: 
-	D3DKMT_BRIGHTNESS_INFO_TYPE
product: Windows
targetos: Windows
req.typenames: D3DKMT_BRIGHTNESS_INFO_TYPE
---

# _D3DKMT_BRIGHTNESS_INFO_TYPE enumeration


## -description


Indicates the type of information to retrieve or set for the brightness of an integrated display panel.


## -syntax


````
typedef enum _D3DKMT_BRIGHTNESS_INFO_TYPE { 
  D3DKMT_BRIGHTNESS_INFO_GET_POSSIBLE_LEVELS  = 1,
  D3DKMT_BRIGHTNESS_INFO_GET                  = 2,
  D3DKMT_BRIGHTNESS_INFO_SET                  = 3,
  D3DKMT_BRIGHTNESS_INFO_GET_CAPS             = 4,
  D3DKMT_BRIGHTNESS_INFO_SET_STATE            = 5,
  D3DKMT_BRIGHTNESS_INFO_SET_OPTIMIZATION     = 6,
  D3DKMT_BRIGHTNESS_INFO_GET_REDUCTION        = 7,
  D3DKMT_BRIGHTNESS_INFO_BEGIN_MANUAL_MODE    = 8,
  D3DKMT_BRIGHTNESS_INFO_END_MANUAL_MODE      = 9,
  D3DKMT_BRIGHTNESS_INFO_TOGGLE_LOGGING       = 10
} D3DKMT_BRIGHTNESS_INFO_TYPE;
````


## -enum-fields




### -field D3DKMT_BRIGHTNESS_INFO_GET_POSSIBLE_LEVELS

Retrieve all possible brightness levels that the integrated display panel supports.


### -field D3DKMT_BRIGHTNESS_INFO_GET

Retrieve the currently active brightness level.


### -field D3DKMT_BRIGHTNESS_INFO_SET

 Set a new brightness level.


### -field D3DKMT_BRIGHTNESS_INFO_GET_CAPS

Retrieve brightness control capabilities of the integrated display panel.


### -field D3DKMT_BRIGHTNESS_INFO_SET_STATE

Enable smooth brightness control.


### -field D3DKMT_BRIGHTNESS_INFO_SET_OPTIMIZATION

Set the level of optimization that the display miniport driver uses to control the brightness of the integrated display panel.


### -field D3DKMT_BRIGHTNESS_INFO_GET_REDUCTION

Retrieve the current level of backlight reduction that is applied to the integrated display panel.


### -field D3DKMT_BRIGHTNESS_INFO_BEGIN_MANUAL_MODE

The user has begun to manually adjust the brightness level.


### -field D3DKMT_BRIGHTNESS_INFO_END_MANUAL_MODE

The user has ended the manual adjustment of the brightness level.


### -field D3DKMT_BRIGHTNESS_INFO_TOGGLE_LOGGING

Enable or disable Event Tracing for Windows (ETW) logging of brightness information.

