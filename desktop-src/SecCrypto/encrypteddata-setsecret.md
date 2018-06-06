---
Description: Sets the value of the secret used to derive the cryptographic session key used to encrypt and decrypt data.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData.SetSecret method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# EncryptedData.SetSecret method

\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP. Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages. For information about PInvoke, see [Platform Invoke Tutorial](http://go.microsoft.com/fwlink/p/?linkid=119531). The [.NET and CryptoAPI via P/Invoke: Part 1](http://go.microsoft.com/fwlink/p/?linkid=119533) and [.NET and CryptoAPI via P/Invoke: Part 2](http://go.microsoft.com/fwlink/p/?linkid=119534) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](http://go.microsoft.com/fwlink/p/?linkid=119532) may also be helpful.\]

The **SetSecret** method sets the value of the secret used to derive the cryptographic [*session key*](security.s_gly#-security-session-key-gly) used to encrypt and decrypt data.

## Syntax


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## Parameters

<dl> <dt>

*newVal* \[in\]
</dt> <dd>

A string that contains a secret used to create a session cryptographic key.

</dd> <dt>

*SecretType* \[in, optional\]
</dt> <dd>

A value of the [**CAPICOM\_SECRET\_TYPE**](capicom-secret-type.md) enumeration that indicates the kind of secret used to generate the session key. The default value is CAPICOM\_SECRET\_PASSWORD. This parameter can be the following value.



| Value                                                                                                                                                                                        | Meaning                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**CAPICOM\_SECRET\_PASSWORD**</dt> </dl> | The encryption key is to be derived from a password.<br/> |



 

</dd> </dl>

## Return value

This method does not return a value.

## Remarks

The secret is used to create the session key for encryption or decryption. The same secret must be used for both operations. If the secret used to encrypt data is lost, the encrypted data cannot be decrypted.

If appropriate for your application, consider using [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) or [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) to protect the secret before and after use. Clear the memory associated with the secret when done.

## Requirements



|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| End of client support<br/> | Windows Vista<br/>                                                               |
| End of server support<br/> | Windows Server 2008<br/>                                                         |
| Redistributable<br/>       | CAPICOM 2.0 or later on Windows Server 2003 and Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## See also

<dl> <dt>

[**Cryptography Objects**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 



