---
UID: NI:hidclass.IOCTL_HID_SET_DRIVER_CONFIG
title: IOCTL_HID_SET_DRIVER_CONFIG
author: windows-driver-content
description: The IOCTL_HID_SET_DRIVER_CONFIG request sets the driver configuration.
old-location: hid\ioctl_hid_set_driver_config.htm
old-project: hid
ms.assetid: E20A1105-CB86-4CE3-91A4-23B08B4D0393
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: hid.ioctl_hid_set_driver_config, IOCTL_HID_SET_DRIVER_CONFIG control code [Human Input Devices], IOCTL_HID_SET_DRIVER_CONFIG, hidclass/IOCTL_HID_SET_DRIVER_CONFIG
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: hidclass.h
req.include-header: Hidclass.h
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
-	hidclass.h
apiname: 
-	IOCTL_HID_SET_DRIVER_CONFIG
product: Windows
targetos: Windows
req.typenames: *PHDAUDIO_STREAM_FORMAT, HDAUDIO_STREAM_FORMAT
---

# IOCTL_HID_SET_DRIVER_CONFIG IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The <b>IOCTL_HID_SET_DRIVER_CONFIG</b> 
   request sets the driver configuration.

This IOCTL is reserved for system use.


## -ioctlparameters




### -input-buffer


<text></text>



### -input-buffer-length


<text></text>



### -output-buffer


<text></text>



### -output-buffer-length


<text></text>



### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block


Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.
Otherwise, Status to the appropriate error condition as a NTSTATUS code. 
For more information, see [XREF-LINK:NTSTATUS Values].


