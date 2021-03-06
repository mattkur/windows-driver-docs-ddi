---
UID: NS:ntddk._WHEA_XPF_CACHE_CHECK
title: _WHEA_XPF_CACHE_CHECK
author: windows-driver-content
description: The WHEA_XPF_CACHE_CHECK union describes cache error information for an x86 or x64 processor.
old-location: whea\whea_xpf_cache_check.htm
old-project: whea
ms.assetid: 61dd30b9-5290-4c72-b053-586066c58108
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: PWHEA_XPF_CACHE_CHECK, PWHEA_XPF_CACHE_CHECK union pointer [WHEA Drivers and Applications], whea.whea_xpf_cache_check, WHEA_XPF_CACHE_CHECK, *PWHEA_XPF_CACHE_CHECK, ntddk/PWHEA_XPF_CACHE_CHECK, _WHEA_XPF_CACHE_CHECK, WHEA_XPF_CACHE_CHECK union [WHEA Drivers and Applications], ntddk/WHEA_XPF_CACHE_CHECK, whearef_354fb32d-8724-4d6e-acc4-6d1a4cfd77a0.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddk.h
req.include-header: Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Supported in Windows Server 2008, Windows Vista SP1, and later versions of Windows.
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
-	ntddk.h
apiname: 
-	WHEA_XPF_CACHE_CHECK
product: Windows
targetos: Windows
req.typenames: WHEA_XPF_CACHE_CHECK, *PWHEA_XPF_CACHE_CHECK
---

# _WHEA_XPF_CACHE_CHECK structure


## -description


The WHEA_XPF_CACHE_CHECK union describes cache error information for an x86 or x64 processor.


## -syntax


````
typedef union _WHEA_XPF_CACHE_CHECK {
  struct {
    ULONGLONG TransactionTypeValid  :1;
    ULONGLONG OperationValid  :1;
    ULONGLONG LevelValid  :1;
    ULONGLONG ProcessorContextCorruptValid  :1;
    ULONGLONG UncorrectedValid  :1;
    ULONGLONG PreciseIPValid  :1;
    ULONGLONG RestartableIPValid  :1;
    ULONGLONG OverflowValid  :1;
    ULONGLONG ReservedValid  :8;
    ULONGLONG TransactionType  :2;
    ULONGLONG Operation  :4;
    ULONGLONG Level  :3;
    ULONGLONG ProcessorContextCorrupt  :1;
    ULONGLONG Uncorrected  :1;
    ULONGLONG PreciseIP  :1;
    ULONGLONG RestartableIP  :1;
    ULONGLONG Overflow  :1;
    ULONGLONG Reserved  :34;
  };
  ULONGLONG XpfCacheCheck;
} WHEA_XPF_CACHE_CHECK, *PWHEA_XPF_CACHE_CHECK;
````


## -struct-fields




### -field DUMMYSTRUCTNAME

 


### -field DUMMYSTRUCTNAME.TransactionTypeValid

 


### -field DUMMYSTRUCTNAME.OperationValid

 


### -field DUMMYSTRUCTNAME.LevelValid

 


### -field DUMMYSTRUCTNAME.ProcessorContextCorruptValid

 


### -field DUMMYSTRUCTNAME.UncorrectedValid

 


### -field DUMMYSTRUCTNAME.PreciseIPValid

 


### -field DUMMYSTRUCTNAME.RestartableIPValid

 


### -field DUMMYSTRUCTNAME.OverflowValid

 


### -field DUMMYSTRUCTNAME.ReservedValid

 


### -field DUMMYSTRUCTNAME.TransactionType

 


### -field DUMMYSTRUCTNAME.Operation

 


### -field DUMMYSTRUCTNAME.Level

 


### -field DUMMYSTRUCTNAME.ProcessorContextCorrupt

 


### -field DUMMYSTRUCTNAME.Uncorrected

 


### -field DUMMYSTRUCTNAME.PreciseIP

 


### -field DUMMYSTRUCTNAME.RestartableIP

 


### -field DUMMYSTRUCTNAME.Overflow

 


### -field DUMMYSTRUCTNAME.Reserved

 


### -field XpfCacheCheck

A ULONGLONG representation of the contents of the WHEA_XPF_CACHE_CHECK union.


#### - TransactionTypeValid

A single bit that indicates that the <b>TransactionType</b> member contains valid data.


#### - Operation

The type of cache operation that caused the error. Possible values are:



This member contains valid data only if the <b>OperationValid</b> bit is set.


##### - Operation.XPF_CACHE_CHECK_OPERATION_SNOOP

A snoop operation.


#### - TransactionType

The type of transaction that was in progress when the error occurred. Possible values are:



This member contains valid data only if the <b>TransactionTypeValid</b> bit is set.


#### - Overflow

A single bit that indicates that an error overflow occurred.

This member contains valid data only if the <b>OverflowValid</b> bit is set.


#### - UncorrectedValid

A single bit that indicates that the <b>Uncorrected </b>member contains valid data.


#### - LevelValid

A single bit that indicates that the <b>Level</b> member contains valid data.


#### - ProcessorContextCorrupt

A single bit that indicates that the processor context might have been corrupted.

This member contains valid data only if the <b>ProcessorContextCorruptValid</b> bit is set.


##### - TransactionType.XPF_CACHE_CHECK_TRANSACTIONTYPE_DATAACCESS

A data access transaction.


#### - Level

The level of the cache where the error occurred.

This member contains valid data only if the <b>LevelValid</b> bit is set.


#### - RestartableIPValid

A single bit that indicates that the <b>RestartableIP</b> member contains valid data.


##### - Operation.XPF_CACHE_CHECK_OPERATION_EVICTION

An eviction operation.


#### - OperationValid

A single bit that indicates that the <b>Operation</b> member contains valid data.


#### - Uncorrected

A single bit that indicates that the error has not been corrected.

This member contains valid data only if the <b>UncorrectedValid</b> bit is set.


#### - ProcessorContextCorruptValid

A single bit that indicates that the <b>ProcessorContextCorrupt</b> member contains valid data.


#### - RestartableIP

A single bit that indicates that program execution can be restarted reliably at the instruction pointer that is specified in the <b>InstructionPointer</b> member of the <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> union that contains this WHEA_XPF_CACHE_CHECK structure.

This member contains valid data only if the <b>RestartableIPValid</b> bit is set.


##### - TransactionType.XPF_CACHE_CHECK_TRANSACTIONTYPE_GENERIC

A generic transaction.


##### - Operation.XPF_CACHE_CHECK_OPERATION_GENERIC

The type of operation cannot be determined.


##### - Operation.XPF_CACHE_CHECK_OPERATION_DATAREAD

A data read operation.


#### - PreciseIPValid

A single bit that indicates that the <b>PreciseIP</b> member contains valid data.


#### - Reserved

Reserved for system use.


##### - Operation.XPF_CACHE_CHECK_OPERATION_GENWRITE

A generic write operation.


##### - TransactionType.XPF_CACHE_CHECK_TRANSACTIONTYPE_INSTRUCTION

A processor instruction transaction.


##### - Operation.XPF_CACHE_CHECK_OPERATION_INSTRUCTIONFETCH

An instruction fetch operation.


##### - Operation.XPF_CACHE_CHECK_OPERATION_DATAWRITE

A data write operation.


#### - ReservedValid

Reserved for system use.


##### - Operation.XPF_CACHE_CHECK_OPERATION_GENREAD

A generic read operation.


#### - PreciseIP

A single bit that indicates that the instruction pointer that is specified in the <b>InstructionPointer</b> member of the <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> structure that contains this WHEA_XPF_CACHE_CHECK union is directly associated with the error.

This member contains valid data only if the <b>PreciseIPValid</b> bit is set.


#### - OverflowValid

A single bit that indicates that the <b>Overflow</b> member contains valid data.


##### - Operation.XPF_CACHE_CHECK_OPERATION_PREFETCH

An instruction prefetch operation.


## -remarks


If the <b>CheckInfoId</b> member of a <a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a> structure contains WHEA_CACHECHECK_GUID, the <b>CheckInfo</b> member of the WHEA_XPF_PROCINFO structure contains a WHEA_XPF_CACHE_CHECK union.



## -see-also

<a href="..\ntddk\ns-ntddk-_whea_xpf_procinfo.md">WHEA_XPF_PROCINFO</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [whea\whea]:%20WHEA_XPF_CACHE_CHECK union%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

