---
UID: NF:filterpipeline.IPartBase.GetPartCompression
title: IPartBase::GetPartCompression method
author: windows-driver-content
description: The GetPartCompression method gets the compression of the part.
old-location: print\ipartbase_getpartcompression.htm
old-project: print
ms.assetid: 18b2a3c2-26da-434e-bcea-89bd6ef22077
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: IPartBase interface [Print Devices], GetPartCompression method, GetPartCompression, filterpipeline/IPartBase::GetPartCompression, print.ipartbase_getpartcompression, IPartBase::GetPartCompression, GetPartCompression method [Print Devices], IPartBase interface, IPartBase, filterpipeline_384bc679-c974-4c0d-86cd-32cdd0ebf7be.xml, GetPartCompression method [Print Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: filterpipeline.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Filterpipeline.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: filterpipeline.h
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	COM
apilocation: 
-	filterpipeline.h
apiname: 
-	IPartBase.GetPartCompression
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# IPartBase::GetPartCompression method


## -description


The <b>GetPartCompression</b> method gets the compression of the part.


## -syntax


````
HRESULT GetPartCompression(
  [out] EXpsCompressionOptions *pCompression
);
````


## -parameters




### -param pCompression [out]

A pointer to the compression option data for the part.


## -returns


<b>GetPartCompression</b> returns an <b>HRESULT</b> value.


