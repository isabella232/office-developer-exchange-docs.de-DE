---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: Das ConnectingSID-Element stellt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.
ms.openlocfilehash: a30f11721506989a84f52dd04c328974f4483956
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354337"
---
# <a name="connectingsid"></a>ConnectingSID

Das **ConnectingSID** -Element stellt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header. 
  
- [ExchangeImpersonation](exchangeimpersonation.md) 
- [ConnectingSID](connectingsid.md)
  
```xml
<ConnectingSID>
   <PrincipalName/>
</ConnectingSID>
```

```xml
<ConnectingSID>
   <SmtpAddress/>
</ConnectingSID>
```

```xml
<ConnectingSID>
    <SID/> 
</ConnectingSID>
```

```xml
<ConnectingSID>
   <PrimarySmtpAddress/>
</ConnectingSID>
```

**ConnectingSIDType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PrincipalName](principalname.md) <br/> |Stellt den Benutzerprinzipalnamen (UPN) des Kontos, das für den Identitätswechsel verwenden. Dies sollte dem UPN für die Domäne sein, wenn das Benutzerkonto vorhanden ist.  <br/> |
|[SID](sid.md) <br/> |Stellt Security Descriptor Definition Language (SDDL) Form die Sicherheits-ID (SID) für das Konto für den Identitätswechsel verwenden.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP)-Adresse des Kontos, das für den Exchange-Identitätswechsel verwenden. Wenn die primäre SMTP-Adresse angegeben ist, wird es keinen zusätzlichen Active Directory Directory Service Nachschlagen Kosten, um die SID des Benutzers abzurufen. Es wird empfohlen, dass Sie die SID- oder UPN verwenden, sofern er verfügbar ist.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die Simple Mail Transfer Protocol (SMTP)-Adresse des Kontos, das für den Exchange-Identitätswechsel verwenden. Wenn die SMTP-Adresse angegeben ist, wird es eine zusätzliche Active Directory-Suche, um die SID des Benutzers abzurufen Kosten. Es wird empfohlen, dass Sie die SID- oder UPN verwenden, sofern er verfügbar ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |In den SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das Benutzerkonto zu imitieren, das in der **"ExchangeImpersonation"** -Element enthalten ist.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>Hinweise

Das aufrufende Konto muss die **ms-Exch-Impersonation** direkt auf dem Clientzugriffsserver und das **ms-Exch-MayImpersonate** Recht auf entweder haben die Postfachdatenbank, die das Postfach Identität enthält oder den Active Directory-Benutzer oder Kontakt -Objekt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Server-zu-Server-Autorisierung in Exchange-Webdienste](http://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

