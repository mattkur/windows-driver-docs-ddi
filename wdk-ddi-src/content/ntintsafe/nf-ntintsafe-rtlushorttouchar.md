---
UID: NF:ntintsafe.RtlUShortToUChar
title: RtlUShortToUChar function
author: windows-driver-content
description: Converts a value of type USHORT to a value of type UCHAR.
old-location: kernel\rtlushorttouchar.htm
old-project: kernel
ms.assetid: E288541F-9FE4-4CF6-A576-21620A828C5C
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: kernel.rtlushorttouchar, RtlUShortToUChar, RtlUShortToUChar function [Kernel-Mode Driver Architecture], ntintsafe/RtlUShortToUChar
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntintsafe.h
req.include-header: 
req.target-type: Desktop
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
-	Ntintsafe.h
apiname: 
-	RtlUShortToUChar
product: Windows
targetos: Windows
req.typenames: PUBLIC_OBJECT_TYPE_INFORMATION, *PPUBLIC_OBJECT_TYPE_INFORMATION
---

# RtlUShortToUChar function


## -description


Converts a value of type <b>USHORT</b> to a value of type <b>UCHAR</b>.


## -syntax


````
NTSTATUS RtlUShortToUChar(
  _In_  USHORT usOperand,
  _Out_ UCHAR  *pch
);
````


## -parameters




### -param usOperand [in]

The value to be converted.


### -param pch [out]

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks


This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.


