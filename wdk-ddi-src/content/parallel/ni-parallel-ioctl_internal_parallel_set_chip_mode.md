---
UID: NI:parallel.IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE
title: IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE
author: windows-driver-content
description: The IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE request sets the operating mode of a parallel port.
old-location: parports\ioctl_internal_parallel_set_chip_mode.htm
old-project: parports
ms.assetid: c6bf2f5a-1682-4437-93b1-1a7e5794befd
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: parports.ioctl_internal_parallel_set_chip_mode, IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE control code [Parallel Ports], IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE, parallel/IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE, cisspd_f9ea9799-8d87-44e2-89d6-ae1fc0a4f673.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: parallel.h
req.include-header: Parallel.h
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
-	parallel.h
apiname: 
-	IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE
product: Windows
targetos: Windows
req.typenames: *LPRILGBATOKEN, RILGBATOKEN
---

# IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The <b>IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE</b> request sets the operating mode of a parallel port.

For more information, see <a href="https://msdn.microsoft.com/a22cdeef-4ae7-49f8-b0b5-a4d68feb4235">Setting and Clearing the Communication Mode on a ParallelPort</a>.


## -ioctlparameters




### -input-buffer

The <b>AssociatedIrp.SystemBuffer</b> member points to a <a href="..\parallel\ns-parallel-_parallel_chip_mode.md">PARALLEL_CHIP_MODE</a> structure that the client allocates to input chip mode information. The client sets the <b>ChipMode</b> member to the requested operating mode.


### -input-buffer-length

The <b>Parameters.DeviceIoControl.InputBufferLength</b> member is set to the size, in bytes, of a PARALLEL_CHIP_MODE structure. 


### -output-buffer

None.


### -output-buffer-length

None.


### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block

The <b>Information</b> member is set to zero. 

The <b>Status</b> member is set to one of the generic status values returned by internal device control requests for parallel ports or to one of the following values:




#### -STATUS_BUFFER_TOO_SMALL

The value of the <b>Parameters.DeviceIoControl.InputBufferLength</b> member is less than the size, in bytes, of a PARALLEL_CHIP_MODE structure.


#### -STATUS_INVALID_DEVICE_STATE

The mode is not cleared.


#### -STATUS_NO_SUCH_DEVICE

The requested operating mode is not valid.


## -see-also

<a href="..\parallel\ns-parallel-_parallel_chip_mode.md">PARALLEL_CHIP_MODE</a>

<a href="..\parallel\ni-parallel-ioctl_internal_parallel_clear_chip_mode.md">IOCTL_INTERNAL_PARALLEL_CLEAR_CHIP_MODE</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [parports\parports]:%20IOCTL_INTERNAL_PARALLEL_SET_CHIP_MODE control code%20 RELEASE:%20(12/14/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

