---
UID: NI:pointofservicedriverinterface.IOCTL_POINT_OF_SERVICE_CHECK_HEALTH
title: IOCTL_POINT_OF_SERVICE_CHECK_HEALTH
author: windows-driver-content
description: This I/O control function checks the device health.
old-location: pos\ioctl_point_of_service_check_health.htm
old-project: pos
ms.assetid: b11be48b-e791-4599-80da-2446791f3816
ms.author: windowsdriverdev
ms.date: 1/18/2018
ms.keywords: pos.ioctl_point_of_service_check_health, IOCTL_POINT_OF_SERVICE_CHECK_HEALTH control code, IOCTL_POINT_OF_SERVICE_CHECK_HEALTH, pointofservicedriverinterface/IOCTL_POINT_OF_SERVICE_CHECK_HEALTH
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: pointofservicedriverinterface.h
req.include-header: Pointofservicedriverinterface.h
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
-	pointofservicedriverinterface.h
apiname: 
-	IOCTL_POINT_OF_SERVICE_CHECK_HEALTH
product: Windows
targetos: Windows
req.typenames: PosPropertyId
---

# IOCTL_POINT_OF_SERVICE_CHECK_HEALTH IOCTL


##  Major Code: 


[[XREF-LINK:IRP_MJ_DEVICE_CONTROL]

## -description


This I/O control function checks the device health.


## -ioctlparameters




### -input-buffer

Pointer to the input buffer, a <a href="..\pointofservicecommontypes\ne-pointofservicecommontypes-driverunifiedposhealthchecklevel.md">UnifiedPosHealthCheckLevel</a> variable.


### -input-buffer-length

Size of the input buffer, in bytes. Set to sizeof(<i>UnifiedPosHealthCheckLevel</i>).


### -output-buffer

Pointer to a buffer that receives a <a href="..\pointofservicedriverinterface\ns-pointofservicedriverinterface-_posstringtype.md">PosStringType</a> followed by the contents of the health string.


### -output-buffer-length

Size of the output buffer, in bytes. Set to sizeof(<i>PosStringType</i>) + enough room to hold the health string.


### -in-out-buffer


<text></text>



### -inout-buffer-length


<text></text>



### -status-block

Returns <b>TRUE</b> if successful; otherwise, returns <b>FALSE</b>.

To get extended error information, call <a href="http://go.microsoft.com/fwlink/p/?LinkId=316871">GetLastError</a>. The following is a common error value:




#### -STATUS_NOT_SUPPORTED

The driver does not provide health strings.


## -remarks


<h3><a id="Parameters"></a><a id="parameters"></a><a id="PARAMETERS"></a>Parameters</h3>


