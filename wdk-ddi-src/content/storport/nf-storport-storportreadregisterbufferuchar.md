---
UID: NF:storport.StorPortReadRegisterBufferUchar
title: StorPortReadRegisterBufferUchar function
author: windows-driver-content
description: The StorPortReadRegisterBufferUchar routine reads a value from a specified register address.
old-location: storage\storportreadregisterbufferuchar.htm
old-project: storage
ms.assetid: f633a967-46b5-4532-b372-b9739f2146a2
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: storprt_361bfb77-1197-40cb-81ec-fc198e6454e9.xml, storport/StorPortReadRegisterBufferUchar, StorPortReadRegisterBufferUchar, storage.storportreadregisterbufferuchar, StorPortReadRegisterBufferUchar routine [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: storport.h
req.include-header: Storport.h
req.target-type: Universal
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
req.lib: Storport.lib
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	LibDef
apilocation: 
-	Storport.lib
-	Storport.dll
apiname: 
-	StorPortReadRegisterBufferUchar
product: Windows
targetos: Windows
req.typenames: STOR_SPINLOCK
req.product: Windows 10 or later.
---

# StorPortReadRegisterBufferUchar function


## -description


The <b>StorPortReadRegisterBufferUchar</b> routine reads a value from a specified register address. 


## -syntax


````
STORPORT_API VOID StorPortReadRegisterBufferUchar(
  _In_ PVOID  HwDeviceExtension,
  _In_ PUCHAR Register,
  _In_ PUCHAR Buffer,
  _In_ ULONG  Count
);
````


## -parameters




### -param HwDeviceExtension [in]

Pointer to the hardware device extension.


### -param Register [in]

Pointer to the register where the data is to be read. 


### -param Buffer [in]

Pointer to the buffer that receives the data that is read.


### -param Count [in]

Number of data items to be read. Each data item has a size of <b>sizeof</b>(UCHAR). 


## -returns


None



## -remarks


For more information, see <a href="..\srb\nf-srb-scsiportreadregisterbufferuchar.md">ScsiPortReadRegisterBufferUchar</a>. For a nonbuffered version of this routine, see <a href="..\storport\nf-storport-storportreadregisteruchar.md">StorPortReadRegisterUchar</a>.



## -see-also

<a href="..\storport\nf-storport-storportreadregisteruchar.md">StorPortReadRegisterUchar</a>

<a href="..\srb\nf-srb-scsiportreadregisterbufferuchar.md">ScsiPortReadRegisterBufferUchar</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20StorPortReadRegisterBufferUchar routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

