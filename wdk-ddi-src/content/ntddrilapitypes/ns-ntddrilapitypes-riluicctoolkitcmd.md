---
UID: NS:ntddrilapitypes.RILUICCTOOLKITCMD
title: RILUICCTOOLKITCMD
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\riluicctoolkitcmd.htm
old-project: netvista
ms.assetid: f5fc28df-ee06-4efd-8509-a05ed0ebf322
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: *LPRILUICCTOOLKITCMD, netvista.riluicctoolkitcmd, RILUICCTOOLKITCMD structure [Network Drivers Starting with Windows Vista], ntddrilapitypes/RILUICCTOOLKITCMD, RILUICCTOOLKITCMD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddrilapitypes.h
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
-	ntddrilapitypes.h
apiname: 
-	RILUICCTOOLKITCMD
product: Windows
targetos: Windows
req.typenames: *LPRILUICCTOOLKITCMD, RILUICCTOOLKITCMD
---

# RILUICCTOOLKITCMD structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef struct _RILUICCTOOLKITCMD {
  DWORD    cbSize;
  DWORD    dwSlotIndex;
  BOOL     fTerminalResponseNeeded;
  DWORD    dwDetailsSize;
  BYTE [1] bDetails;
} RILUICCTOOLKITCMD, RILUICCTOOLKITCMD;
````


## -struct-fields




### -field cbSize



### -field dwSlotIndex



### -field fTerminalResponseNeeded



### -field dwDetailsSize



### -field bDetails


