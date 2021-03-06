---
UID: NS:winbio_ioctl._WINBIO_BLANK_PAYLOAD
title: _WINBIO_BLANK_PAYLOAD
author: windows-driver-content
description: The IOCTL_BIOMETRIC_RESET and IOCTL_BIOMETRIC_UPDATE_FIRMWARE IOCTLs return the WINBIO_BLANK_PAYLOAD structure as output.
old-location: biometric\winbio_blank_payload.htm
old-project: biometric
ms.assetid: 0bc28853-1c00-42d3-a269-198093d64dd7
ms.author: windowsdriverdev
ms.date: 12/14/2017
ms.keywords: biometric_ref_4a39daf0-52f5-40bf-abc6-40cd3d866f39.xml, PWINBIO_BLANK_PAYLOAD, *PWINBIO_BLANK_PAYLOAD, winbio_ioctl/WINBIO_BLANK_PAYLOAD, WINBIO_BLANK_PAYLOAD structure [Biometric Devices], PWINBIO_BLANK_PAYLOAD structure pointer [Biometric Devices], WINBIO_BLANK_PAYLOAD, biometric.winbio_blank_payload, winbio_ioctl/PWINBIO_BLANK_PAYLOAD, _WINBIO_BLANK_PAYLOAD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbio_ioctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available in Windows 7 and later versions of Windows.
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
-	winbio_ioctl.h
apiname: 
-	WINBIO_BLANK_PAYLOAD
product: Windows
targetos: Windows
req.typenames: WINBIO_BLANK_PAYLOAD, *PWINBIO_BLANK_PAYLOAD
req.product: Windows 10 or later.
---

# _WINBIO_BLANK_PAYLOAD structure


## -description


The <a href="..\winbio_ioctl\ni-winbio_ioctl-ioctl_biometric_reset.md">IOCTL_BIOMETRIC_RESET</a> and <a href="..\winbio_ioctl\ni-winbio_ioctl-ioctl_biometric_update_firmware.md">IOCTL_BIOMETRIC_UPDATE_FIRMWARE</a> IOCTLs return the WINBIO_BLANK_PAYLOAD structure as output.


## -syntax


````
typedef struct _WINBIO_BLANK_PAYLOAD {
  DWORD   PayloadSize;
  HRESULT WinBioHresult;
} WINBIO_BLANK_PAYLOAD, *PWINBIO_BLANK_PAYLOAD;
````


## -struct-fields




### -field PayloadSize

 The total size of the payload.  This includes the fixed length structure and any variable data at the end.


### -field WinBioHresult

The status detail of the I/O operation.  This is where WINBIO error and information codes will be passed. The following table shows possible values.
<table>
<tr>
<th>Status value</th>
<th>Description</th>
</tr>
<tr>
<td>
S_OK

</td>
<td>
The operation completed successfully.

</td>
</tr>
<tr>
<td>
HRESULT_FROM_NT(STATUS_IO_DEVICE_ERROR)

</td>
<td>
The driver could not gather the necessary information from the device.

</td>
</tr>
<tr>
<td>
WINBIO_E_DEVICE_BUSY

</td>
<td>
The device is in the middle of a vendor-specific operation.  This should only be returned when the device cannot be reset, and the vendor-specific operation cannot be canceled.

</td>
</tr>
</table> 

