---
UID: NF:filterpipeline.IPrintWriteStream.WriteBytes
title: IPrintWriteStream::WriteBytes method
author: windows-driver-content
description: The WriteBytes method writes a specified number of bytes to a stream.
old-location: print\iprintwritestream_writebytes.htm
old-project: print
ms.assetid: d47c836e-a291-4cc2-9688-82526f8bfb8b
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: WriteBytes method [Print Devices], IPrintWriteStream interface, IPrintWriteStream::WriteBytes, filterpipeline/IPrintWriteStream::WriteBytes, filterpipeline_168a03b1-8fdc-4a98-9a5f-5c706fcd401b.xml, print.iprintwritestream_writebytes, WriteBytes method [Print Devices], IPrintWriteStream interface [Print Devices], WriteBytes method, WriteBytes, IPrintWriteStream
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
-	IPrintWriteStream.WriteBytes
product: Windows
targetos: Windows
req.typenames: EXpsFontRestriction
---

# IPrintWriteStream::WriteBytes method


## -description


The <code>WriteBytes</code> method writes a specified number of bytes to a stream.


## -syntax


````
HRESULT WriteBytes(
  [in]  void  pvBuffer,
  [in]  ULONG cbBuffer,
  [out] ULONG *pcbWritten
);
````


## -parameters




### -param pvBuffer [in]

A pointer to the buffer that the bytes will be written from.


### -param cbBuffer [in]

The size of the buffer to be read from.


### -param pcbWritten [out]

A pointer to the number of bytes actually written. 


## -returns


<code>WriteBytes</code> returns an <b>HRESULT</b> value.


