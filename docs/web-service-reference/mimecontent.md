---
title: "' MimeContent '"
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
description: Das Element ' MimeContent ' enthält den ASCII-MIME-Stream eines Objekts, das im Format base64Binary dargestellt ist und unterstützt [RFC2045].
ms.openlocfilehash: 60f2d42f09347611559137c494d93036f1192829
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830465"
---
# <a name="mimecontent"></a>' MimeContent '

Das Element **' MimeContent '** enthält den ASCII-MIME-Stream eines Objekts, das im Format base64Binary dargestellt ist und unterstützt [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt).
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**UTF** <br/> |Wenn festgelegt, der Wert für dieses Attribut vom Server ignoriert wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md) | [Element](item.md) | [MeetingCancellation](meetingcancellation.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md)  |  [ MeetingResponse](meetingresponse.md) | [Nachricht](message-ex15websvcsotherref.md) | [RemoveItem](removeitem.md) | [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Ein Textwert, der einen MIME-Stream base64Binary darstellt ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Der Nachrichteninhalt wird über die folgenden drei Ebenen der Codierung, bevor sie den Wert **' MimeContent '** gespeichert ist: 
  
1. Meldungstext – Dies ist der Textkörper Codierung, z. B. Iso-2022-jp für japanischen Schriftzeichen.
    
2. MIME-Stream – Dies ist die ASCII-Codierung des Texts für das Element **' MimeContent '** Nachricht oder UTF8-Codierung von den Nachrichtentext für das [MimeContentUTF8](mimecontentutf8.md) -Element. 
    
3. XML-Dokument – ist dies stets die base64-codierten ASCII-Stream des MIME-Streams, in dem Zeichen wie '\<', welche zu XML, benötigt werden, werden aus XML-Parser ausgeblendet.
    
Jede Ebene ist unabhängig von der Ebene, die er vorangestellt ist.
  
Das Element **' MimeContent '** möglicherweise die gleichen Daten enthalten, die anderen Eigenschaften, die mit einem Element zurückgegeben werden enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

