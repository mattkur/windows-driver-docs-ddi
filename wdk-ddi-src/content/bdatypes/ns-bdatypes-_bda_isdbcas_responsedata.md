---
UID: NS:bdatypes._BDA_ISDBCAS_RESPONSEDATA
title: _BDA_ISDBCAS_RESPONSEDATA
author: windows-driver-content
description: .
old-location: stream\bda_isdbcas_responsedata.htm
old-project: stream
ms.assetid: 70BD9007-6CA4-49EC-8A30-3544FE62C18E
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: stream.bda_isdbcas_responsedata, BDA_ISDBCAS_RESPONSEDATA, PBDA_ISDBCAS_RESPONSEDATA, bdatypes/BDA_ISDBCAS_RESPONSEDATA, bdatypes/PBDA_ISDBCAS_RESPONSEDATA, PBDA_ISDBCAS_RESPONSEDATA structure pointer [Streaming Media Devices], *PBDA_ISDBCAS_RESPONSEDATA, BDA_ISDBCAS_RESPONSEDATA structure [Streaming Media Devices], _BDA_ISDBCAS_RESPONSEDATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdatypes.h
req.include-header: 
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
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	Bdatypes.h
apiname: 
-	BDA_ISDBCAS_RESPONSEDATA
product: Windows
targetos: Windows
req.typenames: *PBDA_ISDBCAS_RESPONSEDATA, BDA_ISDBCAS_RESPONSEDATA
---

# _BDA_ISDBCAS_RESPONSEDATA structure


## -description





## -syntax


````
typedef struct _BDA_ISDBCAS_RESPONSEDATA {
  PBDARESULT lResult;
  ULONG      ulRequestID;
  ULONG      ulIsdbStatus;
  ULONG      ulIsdbDataSize;
  BYTE       argbIsdbCommandData[MIN_DIMENSION];
} BDA_ISDBCAS_RESPONSEDATA, *PBDA_ISDBCAS_RESPONSEDATA;
````


## -struct-fields




### -field lResult



### -field ulRequestID



### -field ulIsdbStatus



### -field ulIsdbDataSize



### -field argbIsdbCommandData


