---
UID: NF:wdm.IoGetCurrentProcess
title: IoGetCurrentProcess function
author: windows-driver-content
description: The IoGetCurrentProcess routine returns a pointer to the current process.
old-location: kernel\iogetcurrentprocess.htm
old-project: kernel
ms.assetid: 97a5c14f-949a-4455-9109-79355e5dec37
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: IoGetCurrentProcess routine [Kernel-Mode Driver Architecture], wdm/IoGetCurrentProcess, IoGetCurrentProcess, k104_f59c640e-e335-46e0-a6ca-2f672bb6fc35.xml, kernel.iogetcurrentprocess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of Windows.
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: Any level
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	DllExport
apilocation: 
-	NtosKrnl.exe
apiname: 
-	IoGetCurrentProcess
product: Windows
targetos: Windows
req.typenames: WORK_QUEUE_TYPE
req.product: Windows 10 or later.
---

# IoGetCurrentProcess function


## -description


The <b>IoGetCurrentProcess</b> routine returns a pointer to the current process.


## -syntax


````
PEPROCESS  IoGetCurrentProcess(void);
````


## -parameters





## -returns


<b>IoGetCurrentProcess</b> returns a pointer to the current process.



## -remarks


This routine is identical to <a href="https://msdn.microsoft.com/library/windows/hardware/ff559933">PsGetCurrentProcess</a>.



## -see-also

<a href="..\wdm\nf-wdm-psgetcurrentthread.md">PsGetCurrentThread</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20IoGetCurrentProcess routine%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

