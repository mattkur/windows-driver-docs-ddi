---
UID: NE:ntddrilapitypes.RILMSGDCSFLAGS
title: RILMSGDCSFLAGS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilmsgdcsflags.htm
old-project: netvista
ms.assetid: 9c69d290-0cc6-4444-b9cb-a9555526e9ed
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: ntddrilapitypes/RIL_DCSFLAG_INDICATIONACTIVE, RIL_DCSFLAG_DISCARD, RILMSGDCSFLAGS, RILMSGDCSFLAGS enumeration [Network Drivers Starting with Windows Vista], ntddrilapitypes/RIL_DCSFLAG_ALL, netvista.rilmsgdcsflags, ntddrilapitypes/RIL_DCSFLAG_COMPRESSED, RIL_DCSFLAG_INDICATIONACTIVE, ntddrilapitypes/RIL_DCSFLAG_DISCARD, RIL_DCSFLAG_COMPRESSED, ntddrilapitypes/RILMSGDCSFLAGS, RIL_DCSFLAG_ALL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
-	RILMSGDCSFLAGS
product: Windows
targetos: Windows
req.typenames: RILMSGDCSFLAGS
---

# RILMSGDCSFLAGS enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef enum _RILMSGDCSFLAGS { 
  RIL_DCSFLAG_COMPRESSED,
  RIL_DCSFLAG_INDICATIONACTIVE,
  RIL_DCSFLAG_DISCARD,
  RIL_DCSFLAG_ALL
} RILMSGDCSFLAGS;
````


## -enum-fields




### -field RIL_DCSFLAG_NONE



### -field RIL_DCSFLAG_COMPRESSED



### -field RIL_DCSFLAG_INDICATIONACTIVE



### -field RIL_DCSFLAG_DISCARD



### -field RIL_DCSFLAG_ALL


