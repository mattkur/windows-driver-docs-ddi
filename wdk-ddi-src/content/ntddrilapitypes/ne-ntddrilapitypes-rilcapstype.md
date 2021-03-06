---
UID: NE:ntddrilapitypes.RILCAPSTYPE
title: RILCAPSTYPE
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilcapstype.htm
old-project: netvista
ms.assetid: 78f372fc-75b2-47e8-ac3f-818b384c6d97
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: ntddrilapitypes/RIL_CAPSTYPE_NITZNOTIFICATION, netvista.rilcapstype, ntddrilapitypes/RIL_CAPSTYPE_ARG_SMALLEST, RIL_CAPSTYPE_ARG_SMALLEST, RILCAPSTYPE, RIL_CAPSTYPE_ARG_LARGEST, RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION, ntddrilapitypes/RIL_CAPSTYPE_ARG_LARGEST, ntddrilapitypes/RIL_CAPSTYPE_MAX, RIL_CAPSTYPE_CALLSUPPORT, ntddrilapitypes/RIL_CAPSTYPE_RADIOCONFIGURATIONS, RILCAPSTYPE enumeration [Network Drivers Starting with Windows Vista], RIL_CAPSTYPE_PBMAXREAD, RIL_CAPSTYPE_PBSTORELOCATIONS, ntddrilapitypes/RIL_CAPSTYPE_CALLSUPPORT, RIL_CAPSTYPE_RADIOCONFIGURATIONS, ntddrilapitypes/RIL_CAPSTYPE_PERSOLOCKPWDLENGTH, ntddrilapitypes/RILCAPSTYPE, RIL_CAPSTYPE_MAX, ntddrilapitypes/RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION, RIL_CAPSTYPE_NITZNOTIFICATION, RIL_CAPSTYPE_SMSSUPPORT, ntddrilapitypes/RIL_CAPSTYPE_PBSTORELOCATIONS, ntddrilapitypes/RIL_CAPSTYPE_PBMAXREAD, ntddrilapitypes/RIL_CAPSTYPE_SMSSUPPORT, RIL_CAPSTYPE_PERSOLOCKPWDLENGTH
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
-	RILCAPSTYPE
product: Windows
targetos: Windows
req.typenames: RILCAPSTYPE
---

# RILCAPSTYPE enumeration


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.


## -syntax


````
typedef enum _RILCAPSTYPE { 
  RIL_CAPSTYPE_PERSOLOCKPWDLENGTH,
  RIL_CAPSTYPE_PBMAXREAD,
  RIL_CAPSTYPE_PBSTORELOCATIONS,
  RIL_CAPSTYPE_RADIOCONFIGURATIONS,
  RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION,
  RIL_CAPSTYPE_NITZNOTIFICATION,
  RIL_CAPSTYPE_CALLSUPPORT,
  RIL_CAPSTYPE_SMSSUPPORT,
  RIL_CAPSTYPE_ARG_SMALLEST,
  RIL_CAPSTYPE_ARG_LARGEST,
  RIL_CAPSTYPE_MAX
} RILCAPSTYPE;
````


## -enum-fields




### -field RIL_CAPSTYPE_PERSOLOCKSUPPORT



### -field RIL_CAPSTYPE_PERSOLOCKPWDLENGTH



### -field RIL_CAPSTYPE_PBMAXREAD



### -field RIL_CAPSTYPE_PBSTORELOCATIONS



### -field RIL_CAPSTYPE_RADIOCONFIGURATIONS



### -field RIL_CAPSTYPE_SIGNALQUALITYIMPLEMENTATION



### -field RIL_CAPSTYPE_NITZNOTIFICATION



### -field RIL_CAPSTYPE_CALLSUPPORT



### -field RIL_CAPSTYPE_SMSSUPPORT



### -field RIL_CAPSTYPE_ARG_SMALLEST



### -field RIL_CAPSTYPE_ARG_LARGEST



### -field RIL_CAPSTYPE_MAX


