---
UID: NF:ntstrsafe.RtlUnicodeStringCbCopyStringNEx
title: RtlUnicodeStringCbCopyStringNEx function
author: windows-driver-content
description: The RtlUnicodeStringCbCopyStringNEx function copies a string into a UNICODE_STRING structure while limiting the size of the copied string.
old-location: kernel\rtlunicodestringcbcopystringnex.htm
old-project: kernel
ms.assetid: 67c364a7-5cf7-424a-8ba3-ba9a11276f5d
ms.author: windowsdriverdev
ms.date: 1/4/2018
ms.keywords: safestrings_3b90a87b-c560-40e4-809a-c3d1dd1671e8.xml, RtlUnicodeStringCbCopyStringNEx, ntstrsafe/RtlUnicodeStringCbCopyStringNEx, kernel.rtlunicodestringcbcopystringnex, RtlUnicodeStringCbCopyStringNEx function [Kernel-Mode Driver Architecture]
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntstrsafe.h
req.include-header: Ntstrsafe.h
req.target-type: Desktop
req.target-min-winverclnt: Available starting with Windows XP with Service Pack 1 (SP1).
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
req.lib: Ntstrsafe.lib
req.dll: 
req.irql: PASSIVE_LEVEL
topictype: 
-	APIRef
-	kbSyntax
apitype: 
-	LibDef
apilocation: 
-	Ntstrsafe.lib
-	Ntstrsafe.dll
apiname: 
-	RtlUnicodeStringCbCopyStringNEx
product: Windows
targetos: Windows
req.typenames: *PBATTERY_REPORTING_SCALE, BATTERY_REPORTING_SCALE
---

# RtlUnicodeStringCbCopyStringNEx function


## -description


The <b>RtlUnicodeStringCbCopyStringNEx</b> function copies a string into a <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure while limiting the size of the copied string.


## -syntax


````
NTSTATUS RtlUnicodeStringCbCopyStringNEx(
  _Out_     PUNICODE_STRING  DestinationString,
  _In_      NTSTRSAFE_PCWSTR pszSrc,
  _In_      size_t           cbToCopy,
  _Out_opt_ PUNICODE_STRING  RemainingString,
  _In_      DWORD            dwFlags
);
````


## -parameters




### -param DestinationString [out]

Optional. A pointer to a <b>UNICODE_STRING</b> structure that receives the copied string. The string that the <i>pszSrc </i>parameter points to (excluding the terminating null) is copied into the buffer that the <i>DestinationString</i> parameter's <b>UNICODE_STRING</b> structure points to. The maximum number of bytes in the string is NTSTRSAFE_UNICODE_STRING_MAX_CCH * sizeof(WCHAR). <i>DestinationString</i> can be <b>NULL</b>, but only if STRSAFE_IGNORE_NULLS is set in <i>dwFlags</i>.


### -param pszSrc [in]

Optional. A pointer to the string to be copied. This pointer can be <b>NULL</b>, but only if STRSAFE_IGNORE_NULLS is set in <i>dwFlags</i>.


### -param cbToCopy [in]

The number of bytes to be copied from the source to the destination. 


### -param RemainingString [out, optional]

Optional. If the caller supplies a non-<b>NULL</b> pointer to a <b>UNICODE_STRING</b> structure, the function sets this structure's <b>Buffer</b> member to the end of the concatenated string, sets the structure's <b>Length</b> member to zero, and sets the structure's <b>MaximumLength</b> member to the number of bytes that are remaining in the destination buffer. <i>RemainingString</i> can be <b>NULL</b>, but only if STRSAFE_IGNORE_NULLS is set in <i>dwFlags</i>.


### -param dwFlags [in]

One or more flags and, optionally, a fill byte. The flags are defined as follows:




##### - dwFlags.STRSAFE_FILL_BEHIND

If this flag is set and the function succeeds, the low byte of <i>dwFlags</i> is used to fill the portion of the destination buffer that follows the last character in the string.


##### - dwFlags.STRSAFE_IGNORE_NULLS

If this flag is set, the source or destination pointer, or both, can be <b>NULL</b>. <b>RtlUnicodeStringCbCopyStringNEx</b> treats <b>NULL</b> source buffer pointers like empty strings (TEXT("")), which can be copied. <b>NULL</b> destination buffer pointers cannot receive nonempty strings.


##### - dwFlags.STRSAFE_NULL_ON_FAILURE

If this flag is set and the function fails, the destination buffer is set to an empty string (TEXT("")). This operation overwrites any preexisting buffer contents.


##### - dwFlags.STRSAFE_ZERO_LENGTH_ON_FAILURE

If this flag is set and the function returns STATUS_BUFFER_OVERFLOW, the destination string length is set to zero bytes.


##### - dwFlags.STRSAFE_FILL_ON_FAILURE

If this flag is set and the function fails, the low byte of <i>dwFlags</i> is used to fill the entire destination buffer. This operation overwrites any preexisting buffer contents.


##### - dwFlags.STRSAFE_NO_TRUNCATION

If this flag is set and the function returns STATUS_BUFFER_OVERFLOW, the contents of the destination buffer are not modified.


## -returns


<b>RtlUnicodeStringCbCopyStringNEx</b> returns one of the following NTSTATUS values.
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
This <i>success</i> status means source data was present, and the strings were concatenated without truncation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
This <i>warning</i> status means that the copy operation did not complete because of insufficient space in the destination buffer. If STRSAFE_NO_TRUNCATION is set in <i>dwFlags</i>, the destination buffer is not modified. If the flag is not set, the destination buffer contains a truncated version of the copied string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
This <i>error</i> status means that the function received an invalid input parameter. For more information, see the following list.

</td>
</tr>
</table> 

<b>RtlUnicodeStringCbCopyStringNEx</b> returns the STATUS_INVALID_PARAMETER value when one of the following occurs:
<ul>
<li>The contents of a <b>UNICODE_STRING</b> structure are invalid.</li>
<li>An invalid flag is specified in <i>dwFlags</i>.</li>
<li>The destination buffer is already full.</li>
<li>A buffer pointer is <b>NULL</b> and the STRSAFE_IGNORE_NULLS flag is not specified in <i>dwFlags</i>.</li>
<li>The destination buffer pointer is <b>NULL</b>, but the buffer size is not zero.</li>
<li>The destination buffer pointer is <b>NULL</b>, or its length is zero, but a nonzero length source string is present.</li>
<li>The <i>cbToCopy</i> parameter's value is greater than NTSTRSAFE_UNICODE_STRING_MAX_CCH * sizeof(WCHAR).</li>
</ul>For information about how to test NTSTATUS values, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565436">Using NTSTATUS Values</a>.



## -remarks


The <b>RtlUnicodeStringCbCopyStringNEx</b> function uses the destination buffer's size to ensure that the copy operation does not write past the end of the buffer. By default, the function does <u>not</u> terminate the resultant string with a null character value (that is, with zero). As an option, the caller can use the STRSAFE_FILL_BEHIND flag and a fill byte value of zero to null-terminate a resultant string that does not occupy the entire destination buffer.

<b>RtlUnicodeStringCbCopyStringNEx</b> adds to the functionality of the <a href="..\ntstrsafe\nf-ntstrsafe-rtlunicodestringcbcopystringn.md">RtlUnicodeStringCbCopyStringN</a> function by returning a <a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a> structure that identifies the end of the destination string and the number of bytes left unused in that string. You can pass flags <b>RtlUnicodeStringCbCopyStringNEx</b> for additional control.

If the source and destination strings overlap, the behavior of the function is undefined.

The <i>pszSrc</i> and <i>DestinationString</i> pointers cannot be <b>NULL</b> unless the STRSAFE_IGNORE_NULLS flag is set in <i>dwFlags</i>. If STRSAFE_IGNORE_NULLS is set, one or both of these pointers can be <b>NULL</b>. If the <i>DestinationString</i> pointer is <b>NULL</b>, the <i>pszSrc</i> pointer must be <b>NULL</b> or point to an empty string.

For more information about the safe string functions, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff565508">Using Safe String Functions</a>.



## -see-also

<a href="..\ntstrsafe\nf-ntstrsafe-rtlunicodestringcbcopystringn.md">RtlUnicodeStringCbCopyStringN</a>

<a href="..\ntstrsafe\nf-ntstrsafe-rtlunicodestringcchcopystringnex.md">RtlUnicodeStringCchCopyStringNEx</a>

<a href="..\wudfwdm\ns-wudfwdm-_unicode_string.md">UNICODE_STRING</a>

 

 

<a href="mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback [kernel\kernel]:%20RtlUnicodeStringCbCopyStringNEx function%20 RELEASE:%20(1/4/2018)&amp;body=%0A%0APRIVACY STATEMENT%0A%0AWe use your feedback to improve the documentation. We don't use your email address for any other purpose, and we'll remove your email address from our system after the issue that you're reporting is fixed. While we're working to fix this issue, we might send you an email message to ask for more info. Later, we might also send you an email message to let you know that we've addressed your feedback.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx." title="Send comments about this topic to Microsoft">Send comments about this topic to Microsoft</a>

