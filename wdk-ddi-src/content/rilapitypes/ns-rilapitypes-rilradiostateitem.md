---
UID: NS:rilapitypes.RILRADIOSTATEITEM
title: RILRADIOSTATEITEM
author: windows-driver-content
description: This topic supports the Windows driver infrastructure and is not intended to be used directly from your code.
old-location: netvista\rilradiostateitem_2.htm
old-project: netvista
ms.assetid: 1cfc3e62-3398-435a-b603-fb7638ed8ce9
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: netvista.rilradiostateitem_2, rilapitypes/RILRADIOSTATEITEM, *LPRILRADIOSTATEITEM, RILRADIOSTATEITEM, RILRADIOSTATEITEM structure [Network Drivers Starting with Windows Vista]
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
-	RILRADIOSTATEITEM
product: Windows
targetos: Windows
req.typenames: RILRADIOSTATEITEM, *LPRILRADIOSTATEITEM
req.product: Windows 10 or later.
---

# RILRADIOSTATEITEM structure


## -description


This topic supports the Windows driver infrastructure and is not intended to be used directly from your code. 


## -syntax


````
typedef struct _RILRADIOSTATEITEM {
  DWORD                                        dwItemId;
  RILRADIOSTATEITEMFLAG                        dwItemFlag;
  DWORD                                        dwItemAttributes;
  NULL                                         RILITEMVALUEUNION;
  RILITEMVALUEUNION                            itemValueUnion;
  NULL                                         switch_is;
  NULL                                         dwItemFlag;
  int                                          intVal;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_INTVAL;
  unsigned int                                 uintVal;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_UINTVAL;
  WCHAR [MAXLENGTH_RADIOITEMVALUE_WCHAR]       wszVal;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_WSZVAL;
  int [MAXLENGTH_RADIOITEMVALUE_INT]           intArray;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_INTARRAY;
  unsigned int [MAXLENGTH_RADIOITEMVALUE_UINT] uintArray;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_UINTARRAY;
  BYTE [MAXLENGTH_RADIOITEMVALUE_BYTE]         byteArray;
  NULL                                         case;
  NULL                                         RIL_RADIOSTATE_ITEMFLAG_USE_BYTEARRAY;
  WCHAR [MAXLENGTH_RADIOITEMNAME]              wszFriendlyName;
  WCHAR [MAXLENGTH_RADIOITEM_OPTIONS]          wszItemValueOptions;
} RILRADIOSTATEITEM, RILRADIOSTATEITEM;
````


## -struct-fields




### -field itemValueUnion



### -field itemValueUnion.intVal

 


### -field itemValueUnion.uintVal

 


### -field itemValueUnion.wszVal

 


### -field itemValueUnion.intArray

 


### -field itemValueUnion.uintArray

 


### -field itemValueUnion.byteArray

 


### -field RILITEMVALUEUNION



### -field dwItemId



### -field dwItemFlag



### -field dwItemAttributes



### -field wszFriendlyName



### -field wszItemValueOptions



#### - byteArray



#### - RIL_RADIOSTATE_ITEMFLAG_USE_UINTARRAY



#### - RIL_RADIOSTATE_ITEMFLAG_USE_BYTEARRAY



#### - uintArray



#### - case



#### - uintVal



#### - switch_is



#### - intArray



#### - intVal



#### - RIL_RADIOSTATE_ITEMFLAG_USE_INTVAL



#### - RIL_RADIOSTATE_ITEMFLAG_USE_INTARRAY



#### - RIL_RADIOSTATE_ITEMFLAG_USE_UINTVAL



#### - RIL_RADIOSTATE_ITEMFLAG_USE_WSZVAL



#### - wszVal


