---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: Das MimeContent-Element enthält den ASCII-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und [RFC2045] unterstützt.
ms.openlocfilehash: 039ef1245d48e4cf13141970921dd210f4bd7d06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530436"
---
# <a name="mimecontent"></a>MimeContent

Das **MimeContent** -Element enthält den ASCII-MIME-Stream eines Objekts, das im base64Binary-Format dargestellt wird und [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)unterstützt.
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**CharacterSet** <br/> |Wenn festgelegt, wird der Wert für dieses Attribut vom Server ignoriert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[CalendarItem](calendaritem.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)  |  [Element](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Ein Textwert, der einen base64Binary-MIME-Stream darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Der Nachrichteninhalt durchläuft die folgenden drei Codierungs stufen, bevor er im **MimeContent** -Wert gespeichert wird: 
  
1. Nachrichtentext: Dies ist die Textcodierung, beispielsweise ISO-2022-JP für japanische Zeichen.
    
2. MIME-Stream: Dies ist die ASCII-Codierung des Nachrichtentexts für das **MimeContent** -Element oder die UTF8-Codierung des Nachrichtentexts für das [MimeContentUTF8](mimecontentutf8.md) -Element. 
    
3. XML-Dokument: Dies ist immer der Base64-codierte ASCII-Datenstrom des MIME-Streams, bei dem Zeichen wie ' \< ', die für XML relevant sind, von XML-Parsern ausgeblendet werden.
    
Jede Ebene ist unabhängig von der vorausgehenden Ebene.
  
Das **MimeContent** -Element kann dieselben Daten enthalten, die andere Eigenschaften, die mit einem Element zurückgegeben werden, enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

