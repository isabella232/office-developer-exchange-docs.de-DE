---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: SmtpAddress-Element stellt die Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für den Identitätswechsel verwendet werden oder Simple Mail Transfer Protocol (SMTP) Empfängeradresse eines Kalenders oder Kontakt Freigabeanfrage dar.
ms.openlocfilehash: 39588f0892cdcec819a1972547155730be5785f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831511"
---
# <a name="smtpaddress"></a>SmtpAddress

**SmtpAddress** -Element stellt die Simple Mail Transfer Protocol (SMTP)-Adresse eines Kontos für den Identitätswechsel verwendet werden oder Simple Mail Transfer Protocol (SMTP) Empfängeradresse eines Kalenders oder Kontakt Freigabeanfrage dar. 
  
```xml
<SmtpAddress/>
```

**SmtpAddressType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConnectingSID](connectingsid.md) <br/> |Gibt ein Konto Identitätswechsel bei Verwendung der "ExchangeImpersonation" SOAP-Header.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[InvalidRecipient](invalidrecipient.md) <br/> |Stellt einen ungültigen Empfänger für einen zum Freigeben von Kalendern oder Kontakt Freigabenachricht an.  <br/> |
|[Empfänger (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Stellt eine Sammlung von Empfängern, die Zugriff auf den freigegebenen Ordner gewährt werden soll.  <br/> |
|[GetSharingFolder](getsharingfolder.md) <br/> |Definiert eine Anforderung an den lokalen Ordner Bezeichner eines angegebenen freigegebenen Ordners abzurufen.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle IIS-Verzeichnis, dass Hosts Exchange-Webdienste des Computers, auf dem Microsoft Exchange Server ausgeführt wird die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

