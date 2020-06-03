---
title: Message (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: Das Message-Element enthält die Abwesenheitsantwort (Out of Office).
ms.openlocfilehash: 13d118422ccb5a2897c21b6d124f170bf461dbf6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467004"
---
# <a name="message-availability"></a>Message (Verfügbarkeit)

Das **Message** -Element enthält die Abwesenheitsantwort (Out of Office). 
  
```xml
<Message/> 
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InternalReply](internalreply.md) <br/> | Enthält die Abwesenheitsnachricht, die an andere Benutzer in der Domäne des Absenders gesendet wird. <br/> <br/>  Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben: <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[ExternalReply](externalreply.md) <br/> | Enthält die Abwesenheitsnachricht, die an Adressen außerhalb der Domäne des Absenders gesendet wird.  <br/> <br/> Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben:  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[ReplyBody](replybody.md) <br/> |Enthält eine Abwesenheitsnachricht und die für die Nachricht verwendete Sprache.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich, um die Abwesenheitsnachricht festzulegen.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer [SetUserOofSettings-Vorgangs](setuseroofsettings-operation.md) Anforderung wird die [OofState](oofstate.md) auf " **aktiviert**" festgelegt, die Dauer von OOF auf 10 Tage festgelegt und die internen und externen Abwesenheitsnachrichten festgelegt.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

