---
title: Dauer (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: The Duration element specifies the duration that the out of office (OOF) status is enabled if the OofState element is set to Scheduled.
ms.openlocfilehash: cb6529bfe3799ff41550d7fe3ce2c79b8a4197e2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544157"
---
# <a name="duration-useroofsettings"></a>Dauer (UserOofSettings)

Das **Duration** -Element gibt die Dauer an, für die der Abwesenheitsstatus (OOF) aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Geplant** festgelegt ist.
  
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
|[StartTime](starttime.md) <br/> |Stellt den Anfang der Zeitspanne dar, die mit einem OOF-Status festgelegt wurde. Dieses Element ist erforderlich.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende der Zeitspanne dar, die mit einem OOF-Status festgelegt wurde. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |Gibt die OOF-Einstellungen an.  <br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.<br/><br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Definiert die OOF-Antwortnachricht (Out of Office) und eine Dauer für das Senden der Antwortnachricht für ein Postfach.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der **Duration-Typ** ist auch der Typ für die Elemente [DetailedSuggestionsWindow,](detailedsuggestionswindow.md) [TimeWindow](timewindow.md)und [OutOfOffice.](outofoffice.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel einer [SetUserOofSettings-Vorgangsanforderung](setuseroofsettings-operation.md) wird [OofState](oofstate.md) auf **Aktiviert,** die internen und externen OOF-Nachrichten und die Dauer von OOF für 10 Tage festgelegt.
  
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

