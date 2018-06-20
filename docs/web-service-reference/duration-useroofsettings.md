---
title: Dauer (' UserOofSettings ')
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
description: Das Dauer-Element gibt die Dauer, die außerhalb der Abwesenheitsstatus (OOF) aktiviert ist, wenn das Element OofState auf geplante Tasks festgelegt ist.
ms.openlocfilehash: 62a5492372fd80173d58e965376b7c8c466825a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758119"
---
# <a name="duration-useroofsettings"></a>Dauer (' UserOofSettings ')

Das **Dauer** -Element gibt die Dauer, die außerhalb der Abwesenheitsstatus (OOF) aktiviert ist, wenn das Element [OofState](oofstate.md) **geplant**festgelegt ist.
  
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
|[StartTime](starttime.md) <br/> |Stellt den Anfang des Zeitraums mit dem Abwesenheitsstatus in festgelegt. Dieses Element ist erforderlich.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende der Zeitspanne, die mit dem Abwesenheitsstatus in festgelegt. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[' UserOofSettings '](useroofsettings.md) <br/> |Gibt die OOF-Einstellungen.  <br/><br/>Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |Enthält die OOF-Einstellungen.<br/><br/>Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[OutOfOffice](outofoffice.md) <br/> |Definiert die Antwortnachricht Out of Office (ABWESEND) und eine Dauer für das Senden der Antwortnachricht für ein Postfach.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Dauer** ist auch der Typ für die Elemente [DetailedSuggestionsWindow](detailedsuggestionswindow.md) [Zeitfenster](timewindow.md)und [OutOfOffice](outofoffice.md) . 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird eine Anforderung [SetUserOofSettings Vorgang](setuseroofsettings-operation.md) legt die [OofState](oofstate.md) auf **aktiviert**, die internen und externen OOF-Nachrichten und die Dauer der OOF für 10 Tage.
  
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
        <SetByLegacyClient>false</SetByLegacyClient>
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

- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)  
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)

