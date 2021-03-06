---
UID: NI:hidclass.IOCTL_HID_ENABLE_SECURE_READ
title: IOCTL_HID_ENABLE_SECURE_READ
author: windows-driver-content
description: The IOCTL_HID_ENABLE_SECURE_READ request enables a secure read for open files of a HID collection.
old-location: hid\ioctl_hid_enable_secure_read.htm
old-project: hid
ms.assetid: 9ec1c4e9-8c98-4772-8657-3392ff0827b5
ms.author: windowsdriverdev
ms.date: 12/21/2017
ms.keywords: hid.ioctl_hid_enable_secure_read, IOCTL_HID_ENABLE_SECURE_READ control code [Human Input Devices], IOCTL_HID_ENABLE_SECURE_READ, hidclass/IOCTL_HID_ENABLE_SECURE_READ, hidioreq_2d4e5797-33fb-40dd-bf76-8d81a0d26826.xml
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
-	IOCTL_HID_ENABLE_SECURE_READ
product: Windows
targetos: Windows
req.typenames: *PHDAUDIO_STREAM_FORMAT, HDAUDIO_STREAM_FORMAT
---

# IOCTL_HID_ENABLE_SECURE_READ IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


The IOCTL_HID_ENABLE_SECURE_READ request enables a secure read for open files of a <a href="https://msdn.microsoft.com/2d3efb38-4eba-43db-8cff-9fac30209952">HID collection</a>. Only a "trusted" user-mode application (an application with SeTcbPrivilege privileges) can successfully use this request. Kernel-mode drivers have SeTcbPrivilege privileges by default, but user-mode applications do not.

A client uses an <a href="..\hidclass\ni-hidclass-ioctl_hid_disable_secure_read.md">IOCTL_HID_DISABLE_SECURE_READ</a> request to cancel an enable secure read request.

For information about how to use enable and disable secure read requests to enforce a secure read for a collection, see <a href="https://msdn.microsoft.com/be3c7d1b-195c-4b7f-a404-070b3b265333">Enforcing a Secure Read For a HID Collection</a>.


## -ioctlparameters




### -input-buffer


       None.


### -input-buffer-length

None.


### -output-buffer


       None.


### -output-buffer-length

None.


### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block

The HID class driver sets the <b>Status</b> field of <b>Irp-&gt;IoStatus</b> to STATUS_SUCCESS if the requester has SeTcbPrivilege privileges and the file is valid. Otherwise, it sets the <b>Status</b> field to STATUS_PRIVILEGE_NOT_HELD.


## -see-also

<a href="..\hidclass\ni-hidclass-ioctl_hid_disable_secure_read.md">IOCTL_HID_DISABLE_SECURE_READ</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [hid\hid]:%20IOCTL_HID_ENABLE_SECURE_READ control code%20 RELEASE:%20(12/21/2017)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

