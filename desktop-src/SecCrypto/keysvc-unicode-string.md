---
Description: The KEYSVC\_UNICODE\_STRING structure defines a Unicode string and a maximum length for the string. This structure is used by the RKeyPFXInstall function.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC\_UNICODE\_STRING structure
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: structure
ms.date: 05/31/2018
---

# KEYSVC\_UNICODE\_STRING structure

The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](security.u_gly#-security-unicode-gly) string and a maximum length for the string. This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.

## Syntax


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## Members

<dl> <dt>

**Length**
</dt> <dd>

A **USHORT** value that specifies the length, in bytes, used for **Buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

A pointer to a **USHORT** that represents the Unicode string.

</dd> </dl>

## Requirements



|                                     |                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## See also

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**KEYSVC\_BLOB**](keysvc-blob.md)
</dt> </dl>

 

 



