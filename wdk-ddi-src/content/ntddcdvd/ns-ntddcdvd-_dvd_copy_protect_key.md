---
UID: NS:ntddcdvd._DVD_COPY_PROTECT_KEY
title: _DVD_COPY_PROTECT_KEY
author: windows-driver-content
description: The DVD_COPY_PROTECT_KEY structure is used in conjunction with the IOCTL_DVD_READ_KEY request to execute a report key command of the specified type.
old-location: storage\dvd_copy_protect_key.htm
old-project: storage
ms.assetid: 79f3fdaf-e23a-40ba-a1eb-5428a63cc96a
ms.author: windowsdriverdev
ms.date: 1/10/2018
ms.keywords: ntddcdvd/PDVD_COPY_PROTECT_KEY, DVD_COPY_PROTECT_KEY, _DVD_COPY_PROTECT_KEY, PDVD_COPY_PROTECT_KEY, PDVD_COPY_PROTECT_KEY structure pointer [Storage Devices], structs-DVD_3ea6aa08-28ce-42d0-855d-d2e83ce58f89.xml, DVD_COPY_PROTECT_KEY structure [Storage Devices], storage.dvd_copy_protect_key, ntddcdvd/DVD_COPY_PROTECT_KEY, *PDVD_COPY_PROTECT_KEY
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddcdvd.h
req.include-header: Ntddcdvd.h
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
-	ntddcdvd.h
apiname: 
-	DVD_COPY_PROTECT_KEY
product: Windows
targetos: Windows
req.typenames: *PDVD_COPY_PROTECT_KEY, DVD_COPY_PROTECT_KEY
---

# _DVD_COPY_PROTECT_KEY structure


## -description


The <b>DVD_COPY_PROTECT_KEY</b> structure is used in conjunction with the <a href="..\ntddcdvd\ni-ntddcdvd-ioctl_dvd_read_key.md">IOCTL_DVD_READ_KEY</a> request to execute a report key command of the specified type. 


## -syntax


````
typedef struct _DVD_COPY_PROTECT_KEY {
  ULONG          KeyLength;
  DVD_SESSION_ID SessionId;
  DVD_KEY_TYPE   KeyType;
  ULONG          KeyFlags;
  union {
    HANDLE        FileHandle;
    LARGE_INTEGER TitleOffset;
  } Parameters;
  UCHAR          KeyData[];
} DVD_COPY_PROTECT_KEY, *PDVD_COPY_PROTECT_KEY;
````


## -struct-fields




### -field Parameters



### -field Parameters.FileHandle

Pointer to the file handle for the physical device that the copy protection is being negotiated on.


### -field Parameters.TitleOffset

Contains the logical block address on the media of the title.

The upper layers of the operating system use the <b>FileHandle</b> member. The file system converts the value in <b>FileHandle</b> into a logical block address and stores the result in the <b>TitleOffset</b> member. Kernel-mode drivers use the <b>TitleOffset</b> member.


### -field KeyLength

Indicates the length of the key data to be retrieved. 


### -field SessionId

Indicates the DVD session ID. 


### -field KeyType

Indicates the key type. The DVD device driver uses this information to determine the key format in a report key command, as defined by the <i>SCSI Multimedia Commands - 3 (MMC-3)</i> specification. A report key command either reports key data for a specified key (challenge key, bus key, title key, RPC key, or disk key), reports the state of the authentication success flag (ASF), or invalidates an authentication grant ID (AGID). See the <i>MMC-3</i> specification for further information. 


### -field KeyFlags



### -field KeyData

Contains the key data that was returned. 


####### - KeyFlags.Contains copy generation management system (CGMS) data. For devices that implement a CGMS protection scheme, the CGMS data is returned with the title key data in the KeyFlags member. This member can have any of the following values:



################# - KeyFlags.Value
Meaning



DVD_CGMS_RESERVED_MASK


Mask of reserved bits. 




DVD_CGMS_COPY_PROTECT_MASK


Copy protection bitmask. 




DVD_CGMS_COPY_PERMITTED


Copying is permitted, within limits of copyright restrictions. 




DVD_CGMS_COPY_ONCE


One generation of copies can be made.




DVD_CGMS_NO_COPY


No copying is allowed.




DVD_COPYRIGHT_MASK


Copyright bitmask. 




DVD_NOT_COPYRIGHTED


Copying is permitted without restriction.




DVD_COPYRIGHTED


Data is copyrighted. 




DVD_SECTOR_PROTECT_MASK


Sector protection bitmask. 




DVD_SECTOR_NOT_PROTECTED


Title key data is not encrypted. No decryption necessary. 




DVD_SECTOR_PROTECTED


Title key data must be decrypted.



## -see-also

<a href="..\ntddcdvd\ne-ntddcdvd-dvd_key_type.md">DVD_KEY_TYPE</a>

<a href="..\ntddcdvd\ni-ntddcdvd-ioctl_dvd_read_key.md">IOCTL_DVD_READ_KEY</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [storage\storage]:%20DVD_COPY_PROTECT_KEY structure%20 RELEASE:%20(1/10/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

