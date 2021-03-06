---
UID: NF:ntifs.FsRtlIsAnsiCharacterLegalNtfs
title: FsRtlIsAnsiCharacterLegalNtfs macro
author: windows-driver-content
description: The FsRtlIsAnsiCharacterLegalNtfs macro determines whether an ANSI character is legal for NTFS file names.
old-location: ifsk\fsrtlisansicharacterlegalntfs.htm
old-project: ifsk
ms.assetid: 05d03799-752d-4f59-b96e-1a6d91bee8c4
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: fsrtlref_9150101b-7411-4de2-afd5-0b928ed0e6b1.xml, ntifs/FsRtlIsAnsiCharacterLegalNtfs, FsRtlIsAnsiCharacterLegalNtfs, FsRtlIsAnsiCharacterLegalNtfs function [Installable File System Drivers], ifsk.fsrtlisansicharacterlegalntfs
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: ntifs.h
req.include-header: Ntifs.h
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
req.lib: ntifs.h
req.dll: 
req.irql: Any level
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	ntifs.h
apiname: 
-	FsRtlIsAnsiCharacterLegalNtfs
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlIsAnsiCharacterLegalNtfs macro


## -description


The <b>FsRtlIsAnsiCharacterLegalNtfs</b> macro determines whether an ANSI character is legal for NTFS file names.


## -syntax


````
BOOLEAN FsRtlIsAnsiCharacterLegalNtfs(
   PSCHAR  *Character,
   BOOLEAN WildCardsPermissible
);
````


## -parameters




### -param C

TBD


### -param WILD_OK

TBD




#### - WildCardsPermissible

Set to <b>TRUE</b> if wildcard characters are to be considered legal, <b>FALSE</b> otherwise.


#### - Character

Pointer to the character to be tested.


## -remarks


For information about other string-handling routines, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>. 



## -see-also

<a href="..\ntifs\nf-ntifs-fsrtlisansicharacterlegal.md">FsRtlIsAnsiCharacterLegal</a>

<a href="..\ntifs\nf-ntifs-fsrtlisansicharacterlegalhpfs.md">FsRtlIsAnsiCharacterLegalHpfs</a>

<a href="..\ntifs\nf-ntifs-fsrtlisansicharacterlegalfat.md">FsRtlIsAnsiCharacterLegalFat</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FsRtlIsAnsiCharacterLegalNtfs function%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

