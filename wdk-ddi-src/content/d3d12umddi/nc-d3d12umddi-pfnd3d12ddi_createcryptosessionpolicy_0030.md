---
UID: NC:d3d12umddi.PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030
title: PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030
author: windows-driver-content
description: Used to create a crypto session policy.
old-location: display\pfnd3d12ddi_createcryptosessionpolicy_0030.htm
old-project: display
ms.assetid: BB3B2C57-CE5A-4E15-ABCB-4817C0234B62
ms.author: windowsdriverdev
ms.date: 12/29/2017
ms.keywords: display.pfnd3d12ddi_createcryptosessionpolicy_0030, PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030 callback function [Display Devices], PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030, d3d12umddi/PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d12umddi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
-	d3d12umddi.h
apiname: 
-	PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030
product: Windows
targetos: Windows
req.typenames: D3D11_1DDI_GETCAPTUREHANDLEDATA
---

# PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030 callback


## -description


Used to create a crypto session policy.


## -prototype


````
HRESULT APIENTRY* PFND3D12DDI_CREATECRYPTOSESSIONPOLICY_0030(
             D3D12DDI_HDEVICE                              hDrvDevice,
  _In_ const D3D12DDIARG_CREATE_CRYPTO_SESSION_POLICY_0030 *pArgs,
             D3D12DDI_HCRYPTOSESSION_0030                  hDrvCryptoSession,
             D3D12DDI_HCRYPTOSESSIONPOLICY_0030            hDrvCryptoSessionPolicy,
             D3D12DDI_HRTPROTECTEDSESSION_0030             hRtProtectedSession
);
````


## -parameters




### -param hDrvDevice

The hardware device being processed.


### -param *pArgs



### -param hDrvCryptoSession

Used to create a crypto session.


### -param hDrvCryptoSessionPolicy

Used to create a crypto session policy.


### -param hRtProtectedSession

Used to create a protected session.


#### - pArgs [in]

The arguments used to create a crypto session policy.


## -returns


Returns STATUS_SUCCESS if completed successfully.


