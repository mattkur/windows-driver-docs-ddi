---
UID: NS:fltkernel._FLT_TAG_DATA_BUFFER
title: _FLT_TAG_DATA_BUFFER
author: windows-driver-content
description: The FLT_TAG_DATA_BUFFER structure contains information about a reparse point tag.
old-location: ifsk\flt_tag_data_buffer.htm
old-project: ifsk
ms.assetid: a101e0c8-7121-42b6-aa0e-299f37af8e47
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: *PFLT_TAG_DATA_BUFFER, fltkernel/PFLT_TAG_DATA_BUFFER, FltSystemStructures_47092b0b-5a4b-40eb-8b5f-f0a182d5e509.xml, FLT_TAG_DATA_BUFFER, PFLT_TAG_DATA_BUFFER structure pointer [Installable File System Drivers], fltkernel/FLT_TAG_DATA_BUFFER, ifsk.flt_tag_data_buffer, PFLT_TAG_DATA_BUFFER, FLT_TAG_DATA_BUFFER structure [Installable File System Drivers], _FLT_TAG_DATA_BUFFER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: fltkernel.h
req.include-header: FltKernel.h
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
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	HeaderDef
apilocation: 
-	fltkernel.h
apiname: 
-	FLT_TAG_DATA_BUFFER
product: Windows
targetos: Windows
req.typenames: FLT_TAG_DATA_BUFFER, *PFLT_TAG_DATA_BUFFER
---

# _FLT_TAG_DATA_BUFFER structure


## -description


The FLT_TAG_DATA_BUFFER structure contains information about a reparse point tag. 


## -syntax


````
typedef struct _FLT_TAG_DATA_BUFFER {
  ULONG  FileTag;
  USHORT TagDataLength;
  USHORT UnparsedNameLength;
  union {
    struct {
      USHORT SubstituteNameOffset;
      USHORT SubstituteNameLength;
      USHORT PrintNameOffset;
      USHORT PrintNameLength;
      ULONG  Flags;
      WCHAR  PathBuffer[1];
    } SymbolicLinkReparseBuffer;
    struct {
      USHORT SubstituteNameOffset;
      USHORT SubstituteNameLength;
      USHORT PrintNameOffset;
      USHORT PrintNameLength;
      WCHAR  PathBuffer[1];
    } MountPointReparseBuffer;
    struct {
      UCHAR DataBuffer[1];
    } GenericReparseBuffer;
    struct {
      GUID  TagGuid;
      UCHAR DataBuffer[1];
    } GenericGUIDReparseBuffer;
  };
} FLT_TAG_DATA_BUFFER, *PFLT_TAG_DATA_BUFFER;
````


## -struct-fields




### -field SymbolicLinkReparseBuffer

 


### -field SymbolicLinkReparseBuffer.SubstituteNameOffset

 


### -field SymbolicLinkReparseBuffer.SubstituteNameLength

 


### -field SymbolicLinkReparseBuffer.PrintNameOffset

 


### -field SymbolicLinkReparseBuffer.PrintNameLength

 


### -field SymbolicLinkReparseBuffer.Flags

 


### -field SymbolicLinkReparseBuffer.PathBuffer

 


### -field MountPointReparseBuffer

 


### -field MountPointReparseBuffer.SubstituteNameOffset

 


### -field MountPointReparseBuffer.SubstituteNameLength

 


### -field MountPointReparseBuffer.PrintNameOffset

 


### -field MountPointReparseBuffer.PrintNameLength

 


### -field MountPointReparseBuffer.PathBuffer

 


### -field GenericReparseBuffer

 


### -field GenericReparseBuffer.DataBuffer

 


### -field GenericGUIDReparseBuffer

 


### -field GenericGUIDReparseBuffer.TagGuid

 


### -field GenericGUIDReparseBuffer.DataBuffer

 


### -field FileTag

Reparse point tag. 


### -field TagDataLength

Size, in bytes, of the reparse data pointed to by the <b>DataBuffer</b> member.


### -field UnparsedNameLength

Length, in bytes, of the unparsed portion of the file name pointed to by the <b>FileName</b> member of the associated file object.  For more information about the <b>FileName</b> member, see <a href="..\wdm\ns-wdm-_file_object.md">FILE_OBJECT</a>.


###### - ( unnamed union ).SymbolicLinkReparseBuffer.Flags

If the SYMLINK_FLAG_RELATIVE flag is set, the <b>PathBuffer</b> path is relative to the path contained in the <b>FileName</b> member of the associated file object.


###### - ( unnamed union ).SymbolicLinkReparseBuffer.PrintNameOffset

Offset, in bytes, of the print name string in the <b>PathBuffer</b> array. Note that this offset must be divided by <b>sizeof(</b>WCHAR<b>)</b> to get the array index. 


###### - ( unnamed union ).MountPointReparseBuffer.PathBuffer

First character of the path string. This character is followed in memory by the remainder of the string. 


##### - ( unnamed union ).SymbolicLinkReparseBuffer



###### - ( unnamed union ).MountPointReparseBuffer.PrintNameLength

Length, in bytes, of the print name string. If the print name string is NULL-terminated, <b>PrintNameLength</b> does not include space for the UNICODE_NULL terminator. 


###### - ( unnamed union ).SymbolicLinkReparseBuffer.SubstituteNameLength

Length, in bytes, of the substitute name string. If the substitute name string is NULL-terminated, <b>SubstituteNameLength</b> does not include space for the UNICODE_NULL terminator. 


###### - ( unnamed union ).SymbolicLinkReparseBuffer.SubstituteNameOffset

Offset, in bytes, of the substitute name string in the <b>PathBuffer</b> array. Note that this offset must be divided by <b>sizeof(</b>WCHAR<b>)</b> to get the array index. 


###### - ( unnamed union ).MountPointReparseBuffer.SubstituteNameLength

Length, in bytes, of the substitute name string. If the substitute name string is NULL-terminated, <b>SubstituteNameLength</b> does not include space for the UNICODE_NULL terminator. 


###### - ( unnamed union ).GenericGUIDReparseBuffer.DataBuffer

Pointer to a buffer that contains user-defined data for the reparse point. 


###### - ( unnamed union ).MountPointReparseBuffer.SubstituteNameOffset

Offset, in bytes, of the substitute name string in the <b>PathBuffer</b> array. Note that this offset must be divided by <b>sizeof(</b>WCHAR<b>)</b> to get the array index. 


###### - ( unnamed union ).GenericGUIDReparseBuffer.TagGuid

Globally unique identifier (GUID) that uniquely identifies the type of reparse point. If <b>FileTag</b> is not a Microsoft tag, this member cannot be <b>NULL</b>. 


##### - ( unnamed union ).GenericGUIDReparseBuffer



#### - ( unnamed union )

 


###### - ( unnamed union ).SymbolicLinkReparseBuffer.PathBuffer

First character of the path string. This character is followed in memory by the remainder of the string. 


###### - ( unnamed union ).SymbolicLinkReparseBuffer.PrintNameLength

Length, in bytes, of the print name string. If the print name string is NULL-terminated, <b>PrintNameLength</b> does not include space for the UNICODE_NULL terminator. 


###### - ( unnamed union ).GenericReparseBuffer.DataBuffer

Pointer to a buffer that contains user-defined data for the reparse point. 


##### - ( unnamed union ).MountPointReparseBuffer



###### - ( unnamed union ).MountPointReparseBuffer.PrintNameOffset

Offset, in bytes, of the print name string in the <b>PathBuffer</b> array. Note that this offset must be divided by <b>sizeof(</b>WCHAR<b>)</b> to get the array index. 


##### - ( unnamed union ).GenericReparseBuffer



## -remarks


A minifilter can use the FLT_TAG_DATA_BUFFER structure to store information about a reparse point tag. 

A pointer to an FLT_TAG_DATA_BUFFER structure that contains reparse point tag data for an operation is stored in the <b>TagData</b> member of the <a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a> structure for the operation. 

The FLT_TAG_DATA_BUFFER_HEADER_SIZE macro returns the size of the fixed portion of the FLT_TAG_DATA_BUFFER structure. 



## -see-also

<a href="..\fltkernel\ns-fltkernel-_flt_callback_data.md">FLT_CALLBACK_DATA</a>

<a href="..\fltkernel\nf-fltkernel-flttagfile.md">FltTagFile</a>

<a href="..\wdm\ns-wdm-_file_object.md">FILE_OBJECT</a>

<a href="..\fltkernel\nf-fltkernel-fltuntagfile.md">FltUntagFile</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FLT_TAG_DATA_BUFFER structure%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

