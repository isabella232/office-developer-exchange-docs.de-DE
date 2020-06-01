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
description: Das ConnectingSID-Element stellt ein Konto für den Identitätswechsel dar, wenn Sie den ExchangeImpersonation-SOAP-Header verwenden.
ms.openlocfilehash: f4edf63f129fc769f4a2d710a505b40da4057fab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459279"
---
# <a name="connectingsid"></a>ConnectingSID

Das **ConnectingSID** -Element stellt ein Konto für den Identitätswechsel dar, wenn Sie den ExchangeImpersonation-SOAP-Header verwenden. 
  
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
|[PrincipalName](principalname.md) <br/> |Stellt den Benutzerprinzipalnamen (User Principal Name, UPN) des Kontos dar, das für den Identitätswechsel verwendet werden soll. Dies sollte der UPN für die Domäne sein, in der das Benutzerkonto vorhanden ist.  <br/> |
|[SID](sid.md) <br/> |Stellt das SDDL-Formular (Security Descriptor Definition Language) der Sicherheits-ID (Security Identifier, SID) für das Konto dar, das für den Identitätswechsel verwendet werden soll.  <br/> |
|[PrimarySmtpAddress](primarysmtpaddress.md) <br/> |Stellt die primäre Simple Mail Transfer Protocol (SMTP) Adresse des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll. Wenn die primäre SMTP-Adresse angegeben wird, kostet Sie eine zusätzliche Active Directory Verzeichnisdienstsuche, um die SID des Benutzers zu erhalten. Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.  <br/> |
|[SmtpAddress](smtpaddress.md) <br/> |Stellt die Simple Mail Transfer Protocol (SMTP) Adresse des Kontos dar, das für den Exchange-Identitätswechsel verwendet werden soll. Wenn die SMTP-Adresse angegeben wird, kostet Sie eine zusätzliche Active Directory Suche, um die SID des Benutzers zu erhalten. Es wird empfohlen, die SID oder den UPN zu verwenden, wenn diese verfügbar sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Wird im SOAP-Header einer Anforderung verwendet. Wenn dieses Element vorhanden ist, versucht der Aufrufer, das im **ExchangeImpersonation** -Element enthaltene Konto zu imitieren.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/ExchangeImpersonation` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Anruf Konto muss über das Recht **MS-Wechsel-Wechsel** auf dem Client Zugriffsserver und das **MS-MayImpersonate** direkt in der Postfachdatenbank, die das Postfach enthält, den Identitätswechsel oder das Active Directory Benutzer-oder Kontaktobjekt aufweisen. 
  
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

