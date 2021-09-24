---
title: ConnectingSID
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectingSID
api_type:
- schema
ms.assetid: 56d6aa52-8fa6-4773-9046-44a6f4f5d97c
description: Das ConnectingSID-Element stellt ein Konto dar, das bei Verwendung des EXCHANGEImpersonation-SOAP-Headers als Identitätswechsel verwendet werden soll.
ms.openlocfilehash: 21cfcfc3590ea5a8b8ca5b53dfdb403e108e37f7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515971"
---
# <a name="connectingsid"></a>ConnectingSID

Das **ConnectingSID-Element** stellt ein Konto dar, das bei Verwendung des EXCHANGEImpersonation-SOAP-Headers als Identitätswechsel verwendet werden soll. 
  
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
|[PrincipalName](principalname.md) <br/> |Stellt den Benutzerprinzipalnamen (UPN) des Kontos dar, das für identitätswechsel verwendet werden soll. Dies sollte der UPN für die Domäne sein, in der das Benutzerkonto vorhanden ist.  <br/> |
|[SID](sid.md) <br/> |Stellt die SDDL-Form (Security Descriptor Definition Language) der Sicherheits-ID (SID) für das Konto dar, das für Identitätswechsel verwendet werden soll.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre SMTP-Adresse (Simple Mail Transfer Protocol) des Kontos dar, das für Exchange Identitätswechsel verwendet werden soll. Wenn die primäre SMTP-Adresse angegeben wird, wird eine zusätzliche Active Directory-Verzeichnisdienst-Suche kosten, um die SID des Benutzers abzurufen. Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die SMTP-Adresse (Simple Mail Transfer Protocol) des Kontos dar, das für Exchange Identitätswechsel verwendet werden soll. Wenn die SMTP-Adresse angegeben wird, kostet dies eine zusätzliche Active Directory-Suche, um die SID des Benutzers abzurufen. Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, die Identität des Kontos imItieren, das im **ExchangeImpersonation-Element** enthalten ist.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das aufrufende Konto muss über den **ms-exch-Identitätswechsel** rechts auf dem Clientzugriffsserver und über das **Recht "ms-exch-MayImpersonate"** in der Postfachdatenbank verfügen, die das Postfach zum Identitätswechsel enthält, oder über das Active Directory-Benutzer- oder -Kontaktobjekt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Server-zu-Server-Autorisierung in EWS](https://msdn.microsoft.com/library/f1610a20-672d-448b-8c00-5b0fbcaf31cb%28Office.15%29.aspx)

