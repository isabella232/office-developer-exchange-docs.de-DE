---
title: Dauer (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Das Duration-Element gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das OofState-Element auf Scheduled festgelegt ist.
ms.openlocfilehash: 0ba0f1ea7498781c0cccb072c7ea0fa05414764c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457298"
---
# <a name="duration-useroofsettings"></a>Dauer (UserOofSettings)

Das **Duration** -Element gibt die Dauer an, für die der Abwesenheitsstatus aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 **Duration**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Stellt den Anfang der Zeitspanne fest, die mit einem Abwesenheitsstatus festgelegt wurde. Dieses Element ist erforderlich.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende der Zeitspanne fest, die mit einem Abwesenheitsstatus festgelegt wurde. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Gibt die Abwesenheitseinstellungen an.  <br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.<br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Definiert die Abwesenheit (Out of Office, OOF) Antwortnachricht und eine Dauer für das Senden der Antwortnachricht für ein Postfach.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Typ Duration ist auch der Typ für die Elemente [DetailedSuggestionsWindow](detailedsuggestionswindow.md), **Zeit** [Fenster](timewindow.md)und [OutOfOffice](outofoffice.md) . 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer [SetUserOofSettings-Vorgangs](setuseroofsettings-operation.md) Anforderung wird die [OofState](oofstate.md) auf **Enabled**, die internen und externen Abwesenheitsnachrichten festgelegt und die Dauer von OOF für 10 Tage festgelegt.
  
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
        <SetByLegacyClient>false</SetByLegacyClient>
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

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)  
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

