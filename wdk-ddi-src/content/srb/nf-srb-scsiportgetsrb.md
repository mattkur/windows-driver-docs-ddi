---
UID: NF:srb.ScsiPortGetSrb
title: ScsiPortGetSrb function
author: windows-driver-content
description: The ScsiPortGetSrb routine returns a pointer to an active SCSI request for a particular logical unit.Note  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future.
old-location: storage\scsiportgetsrb.htm
old-project: storage
ms.assetid: c8f0e47c-4d06-445f-a6dd-9bd80fc490bc
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: srb/ScsiPortGetSrb, storage.scsiportgetsrb, scsiprt_28205a6f-8758-4aed-8fae-94a12c216cf4.xml, ScsiPortGetSrb, ScsiPortGetSrb routine [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: srb.h
req.include-header: Miniport.h, Scsi.h
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
req.lib: Scsiport.lib
req.dll: 
req.irql: 
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	LibDef
apilocation: 
-	Scsiport.lib
-	Scsiport.dll
apiname: 
-	ScsiPortGetSrb
product: Windows
targetos: Windows
req.typenames: *PSPB_CONTROLLER_CONFIG, SPB_CONTROLLER_CONFIG
req.product: Windows 10 or later.
---

# ScsiPortGetSrb function


## -description


The <b>ScsiPortGetSrb</b> routine returns a pointer to an active SCSI request for a particular logical unit.
<div class="alert"><b>Note</b>  The SCSI port driver and SCSI miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="https://msdn.microsoft.com/en-us/windows/hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -syntax


````
PSCSI_REQUEST_BLOCK ScsiPortGetSrb(
  _In_ PVOID DeviceExtension,
  _In_ UCHAR PathId,
  _In_ UCHAR TargetId,
  _In_ UCHAR Lun,
  _In_ LONG  QueueTag
);
````


## -parameters




### -param DeviceExtension [in]

Pointer to the miniport driver's per-HBA storage area.


### -param PathId [in]

Identifies the SCSI bus.


### -param TargetId [in]

Identifies the target controller or device on the bus.


### -param Lun [in]

Identifies the logical unit number of the target device.


### -param QueueTag [in]

Specifies the queue tag if the miniport driver handles tagged requests; SP_UNTAGGED indicates that the request is not tagged.


## -returns


<b>ScsiPortGetSrb</b> returns a pointer to a request for the specified logical unit. If there is no outstanding request for the given peripheral or if the <i>QueueTag</i> value is invalid, it returns <b>NULL</b>.



## -see-also

<a href="..\srb\ns-srb-_scsi_request_block.md">SCSI_REQUEST_BLOCK</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20ScsiPortGetSrb routine%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

