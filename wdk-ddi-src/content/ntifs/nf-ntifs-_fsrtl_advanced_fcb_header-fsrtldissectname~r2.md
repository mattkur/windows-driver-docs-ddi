---
UID: NF:ntifs._FSRTL_ADVANCED_FCB_HEADER.FsRtlDissectName~r2
title: FsRtlDissectName function
author: windows-driver-content
description: Given a Unicode pathname string, the FsRtlDissectName routine returns two strings, one containing the first file name found in the string, the other containing the remaining unparsed portion of the pathname string.
old-location: ifsk\fsrtldissectname.htm
old-project: ifsk
ms.assetid: d97de0e1-0724-485d-95da-b9811036a21e
ms.author: windowsdriverdev
ms.date: 1/9/2018
ms.keywords: FsRtlDissectName, FsRtlDissectName routine [Installable File System Drivers], ntifs/FsRtlDissectName, ifsk.fsrtldissectname, fsrtlref_a74da803-0994-46e4-90f7-bc7728b59fe5.xml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntifs.h
req.include-header: Ntifs.h
req.target-type: Universal
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
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	DllExport
apilocation: 
-	NtosKrnl.exe
apiname: 
-	FsRtlDissectName
product: Windows
targetos: Windows
req.typenames: TOKEN_TYPE
---

# FsRtlDissectName function


## -description


Given a Unicode pathname string, the <b>FsRtlDissectName</b> routine returns two strings, one containing the first file name found in the string, the other containing the remaining unparsed portion of the pathname string.


## -syntax


````
VOID FsRtlDissectName(
  _In_  UNICODE_STRING  Path,
  _Out_ PUNICODE_STRING FirstName,
  _Out_ PUNICODE_STRING RemainingName
);
````


## -parameters




### -param Path [in]

Pathname string to be parsed.


### -param FirstName [out]

Pointer to the first file name in the pathname string. 


### -param RemainingName [out]

Pointer to the remaining unparsed portion of the pathname string.


## -returns


None



## -remarks


In the input string, backslashes are read as name separators. The first name in the string is assumed to consist of all characters from the beginning of the string to the character preceding the first backslash, inclusive. There is just one exception to this rule: if the first character in the input string is a backslash, this character is ignored and does not appear in the output string. The remaining portion of the string consists of all characters following the backslash that follows the first name found in the string.

<b>FsRtlDissectName</b> does not check for the presence of illegal characters in the input string.

The following table shows sample input and output values for <b>FsRtlDissectName</b>.  
<table>
<tr>
<th>Path</th>
<th>FirstName</th>
<th>RemainingName</th>
</tr>
<tr>
<td>
empty

</td>
<td>
empty

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A

</td>
<td>
A

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A\B\C\D\E

</td>
<td>
A

</td>
<td>
B\C\D\E

</td>
</tr>
<tr>
<td>
*A?

</td>
<td>
*A?

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
\A

</td>
<td>
A

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A[,]

</td>
<td>
A[,]

</td>
<td>
empty

</td>
</tr>
<tr>
<td>
A\\B+;\C

</td>
<td>
A

</td>
<td>
\B+;\C

</td>
</tr>
</table> 

Note that upon returning, the <b>Buffer</b> members of the output parameters will point into the <b>Buffer</b> member of <b>Path</b>.  Therefore, the caller should not allocate storage for the <b>Buffer</b> members of the two output parameters, as shown in the following example:
<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>.
.
.
/*
The FsRtlDissectName routine will set the members
of the following two structures appropriately:
*/
UNICODE_STRING CurrentComponent;
UNICODE_STRING RemainingComponent;

/*
Do not allocate storage for the Buffer members of CurrentComponent
and RemainingComponent in that they will point into the previoulsy
allocated storage of FullPathName's Buffer member:
*/
FsRtlDissectName (FullPathName, &amp;CurrentComponent, &amp;RemainingComponent);
.
.
.</pre>
</td>
</tr>
</table></span></div>For information about other string-handling routines, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff563884">Strings</a>. 



## -see-also

<a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [ifsk\ifsk]:%20FsRtlDissectName routine%20 RELEASE:%20(1/9/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

