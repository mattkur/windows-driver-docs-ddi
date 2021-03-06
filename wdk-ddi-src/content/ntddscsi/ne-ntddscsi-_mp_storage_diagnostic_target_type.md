---
UID: NE:ntddscsi._MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
title: _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
author: windows-driver-content
description: The MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration specifies the target type of a storage diagnostic.
old-location: storage\mp_storage_diagnostic_target_type.htm
old-project: storage
ms.assetid: 1A48FC0F-7ED2-4F9F-8B61-A498B0D13FE8
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: ntddscsi/StorageDiagnosticTargetTypeHbaFirmware, ntddscsi/MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, *PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, ntddscsi/StorageDiagnosticTargetTypeMiniport, PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, StorageDiagnosticTargetTypeUndefined, MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, ntddscsi/StorageDiagnosticTargetTypeUndefined, ntddscsi/StorageDiagnosticTargetTypePort, StorageDiagnosticTargetTypeHbaFirmware, StorageDiagnosticTargetTypeMax, ntddscsi/StorageDiagnosticTargetTypeMax, _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, storage.mp_storage_diagnostic_target_type, StorageDiagnosticTargetTypePort, ntddscsi/PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE, PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration pointer [Storage Devices], StorageDiagnosticTargetTypeMiniport, MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration [Storage Devices]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: ntddscsi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10, version 1709.
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
-	ntddscsi.h
apiname: 
-	MP_STORAGE_DIAGNOSTIC_TARGET_TYPE
product: Windows
targetos: Windows
req.typenames: MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, *PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE
---

# _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE enumeration


## -description


The <b>MP_STORAGE_DIAGNOSTIC_TARGET_TYPE</b> enumeration specifies the target type of a storage diagnostic.


## -syntax


````
typedef enum _MP_STORAGE_DIAGNOSTIC_TARGET_TYPE { 
  StorageDiagnosticTargetTypeUndefined    = 0,
  StorageDiagnosticTargetTypePort         = 2,
  StorageDiagnosticTargetTypeMiniport,
  StorageDiagnosticTargetTypeHbaFirmware,
  StorageDiagnosticTargetTypeMax
} MP_STORAGE_DIAGNOSTIC_TARGET_TYPE, *PMP_STORAGE_DIAGNOSTIC_TARGET_TYPE;
````


## -enum-fields




### -field MpStorageDiagnosticTargetTypeUndefined



### -field MpStorageDiagnosticTargetTypeMiniport



### -field MpStorageDiagnosticTargetTypeHbaFirmware



### -field MpStorageDiagnosticTargetTypeMax




#### - StorageDiagnosticTargetTypeUndefined

Specifies the target type is undefined.


#### - StorageDiagnosticTargetTypeMax

Specifies the target type is a Max driver.


#### - StorageDiagnosticTargetTypeHbaFirmware

Specifies the target type is a Hba Firmware driver.


#### - StorageDiagnosticTargetTypeMiniport

Specifies the target type is a Miniport driver.


#### - StorageDiagnosticTargetTypePort

Specifies the target type is a port driver.

