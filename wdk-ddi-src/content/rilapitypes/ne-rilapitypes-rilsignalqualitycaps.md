---
UID: NE:rilapitypes.RILSIGNALQUALITYCAPS
title: RILSIGNALQUALITYCAPS
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilsignalqualitycaps_2.htm
old-project: netvista
ms.assetid: 246af8ed-6657-4999-ab9f-a64958a1225d
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: RIL_CAPS_SIGNALQUALITY_MAX, rilapitypes/RIL_CAPS_SIGNALQUALITY_POLLING, netvista.rilsignalqualitycaps_2, rilapitypes/RIL_CAPS_SIGNALQUALITY_MAX, RILSIGNALQUALITYCAPS enumeration [Network Drivers Starting with Windows Vista], rilapitypes/RILSIGNALQUALITYCAPS, RIL_CAPS_SIGNALQUALITY_POLLING, RILSIGNALQUALITYCAPS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: NtosKrnl.exe
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
-	RILSIGNALQUALITYCAPS
product: Windows
targetos: Windows
req.typenames: RILSIGNALQUALITYCAPS
req.product: Windows 10 or later.
---

# RILSIGNALQUALITYCAPS enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef enum _RILSIGNALQUALITYCAPS { 
  RIL_CAPS_SIGNALQUALITY_POLLING,
  RIL_CAPS_SIGNALQUALITY_MAX
} RILSIGNALQUALITYCAPS;
````


## -enum-fields




### -field RIL_CAPS_SIGNALQUALITY_NOTIFICATION



### -field RIL_CAPS_SIGNALQUALITY_POLLING



### -field RIL_CAPS_SIGNALQUALITY_MAX


