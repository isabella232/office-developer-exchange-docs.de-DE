---
title: ExternalReply
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExternalReply
api_type:
- schema
ms.assetid: cbcfa469-242c-4f98-8f4f-2c9bcbe69f5a
description: Das ExternalReply-Element enthält, die Out of Office (OOF)-Antwort, die an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet wird.
ms.openlocfilehash: f318b34c98dd42487b8ca3791ba915fb91d629a5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758397"
---
# <a name="externalreply"></a>ExternalReply

Das **ExternalReply** -Element enthält, die Out of Office (OOF)-Antwort, die an Adressen außerhalb der Domäne oder der vertrauenswürdigen Domänen des Empfängers gesendet wird. 
  
```XML
<ExternalReply>
   <Message/>
</ExternalReply>
```

 **ReplyBody**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|XML: lang  <br/> |Gibt die Sprache, in der Nachricht **ExternalReply** verwendet. Die möglichen Werte für dieses Attribut sind durch IETF RFC 3066 definiert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Nachricht (Verfügbarkeit)](message-availability.md) <br/> |Enthält die Antwort OOF.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[' UserOofSettings '](useroofsettings.md) <br/> |Gibt die OOF-Einstellungen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung SetUserOofSettings legt die [OofState](oofstate.md) auf **aktiviert**, wird die Dauer der OOF auf 10 Tage, und die internen und externen Abwesenheitsnachrichten.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

