---
title: ConversationId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConversationId
api_type:
- schema
ms.assetid: d5f1ddb3-9af3-4677-a6ba-111b304a951e
description: Das ConversationId-Element enthält den Bezeichner eines Elements oder einer Unterhaltung.
ms.openlocfilehash: 345c7c692576abb8c1e1b9848b005ca3d0c0fa0f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547540"
---
# <a name="conversationid"></a>ConversationId

Das **ConversationId-Element** enthält den Bezeichner eines Elements oder einer Unterhaltung. 
  
```XML
<ConversationId Id="" ChangeKey="" />
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Identifiziert ein bestimmtes Element im Exchange Speicher.  <br/> |
|**ChangeKey** <br/> | Identifiziert eine bestimmte Version eines Elements. Für die folgenden Szenarien ist ein **ChangeKey** erforderlich:  <br/><br/>- Das [UpdateItem-Element](updateitem.md) erfordert einen **ChangeKey,** wenn das **ConflictResolution-Attribut** auf AutoResolve festgelegt ist. AutoResolve ist ein Standardwert. Wenn das **ChangeKey -Attribut** nicht enthalten ist, gibt die Antwort einen [ResponseCode](responsecode.md) -Wert gleich **ErrorChangeKeyRequired** zurück.<br/><br/>- [SendItem-,](senditem.md) [DeleteItem-](deleteitem.md)und [DeleteFolder-Elemente](deletefolder.md) erfordern einen **ChangeKey,** um zu testen, ob der versuchte Vorgang auf die neueste Version eines Elements reagiert. Wenn das **ChangeKey** -Attribut nicht in der **ItemId** enthalten ist oder wenn der **ChangeKey** leer ist, gibt die Antwort einen [ResponseCode](responsecode.md) -Wert gleich **ErrorStaleObject** zurück.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[ConversationAction](conversationaction.md) <br/> |Stellt eine einzelne Aktion dar, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Beitragselement im Exchange Informationsspeicher dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindConversation-Vorgang](findconversation-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

