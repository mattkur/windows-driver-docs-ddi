---
UID: NS:rilapitypes.RILCBMSGCONFIG
title: RILCBMSGCONFIG
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcbmsgconfig_2.htm
old-project: netvista
ms.assetid: 7cdab678-5c83-4590-b911-5961db89e7ce
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: *LPRILCBMSGCONFIG, netvista.rilcbmsgconfig_2, RILCBMSGCONFIG, RILCBMSGCONFIG structure [Network Drivers Starting with Windows Vista], rilapitypes/RILCBMSGCONFIG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rilapitypes.h
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
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	rilapitypes.h
apiname: 
-	RILCBMSGCONFIG
product: Windows
targetos: Windows
req.typenames: *LPRILCBMSGCONFIG, RILCBMSGCONFIG
req.product: Windows 10 or later.
---

# RILCBMSGCONFIG structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef struct _RILCBMSGCONFIG {
  DWORD                                   cbSize;
  DWORD                                   dwParams;
  DWORD                                   dwGWLConfigInfoSize;
  RILCBGWLCONFIGINFO [RIL_CB_CONFIG_MAX]  GWLConfigInfo;
  DWORD                                   dwCDMAConfigInfoSize;
  RILCBCDMACONFIGINFO [RIL_CB_CONFIG_MAX] CDMAConfigInfo;
} RILCBMSGCONFIG, RILCBMSGCONFIG;
````


## -struct-fields




### -field cbSize



### -field dwParams



### -field dwGWLConfigInfoSize



### -field GWLConfigInfo



### -field dwCDMAConfigInfoSize



### -field CDMAConfigInfo


