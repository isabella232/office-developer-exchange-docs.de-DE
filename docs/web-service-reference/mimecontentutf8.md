---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: Das MimeContentUTF8-Element enthält den UTF-8-MIME-Stream eines Objekts, das im Format base64Binary dargestellt wird, und unterstützt die e-Mail-Adresse Internationalisierung und [RFC6530].
ms.openlocfilehash: 47599b6634738fd488e5b020f69e36d5fcf550a6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830466"
---
# <a name="mimecontentutf8"></a>MimeContentUTF8

Das **MimeContentUTF8** -Element enthält den UTF-8-MIME-Stream, der ein Objekt, wird im Format base64Binary dargestellt und unterstützt e-Mail-Adresse Internationalisierung und [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt).
  
```XML
<MimeContentUTF8 CharacterSet="" />
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

Ein Textwert, der einen MIME-Stream base64binary darstellt ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Der Nachrichteninhalt wird über die folgenden drei Ebenen der Codierung, bevor sie den Wert des **MimeContentUTF8** gespeichert ist: 
  
1. Meldungstext – Dies ist der Textkörper Codierung, z. B. Iso-2022-jp für japanischen Schriftzeichen.
    
2. MIME-Stream – Dies ist die UTF8-Codierung des Nachrichtentext für das **MimeContentUTF8** -Element oder die ASCII-Codierung von den Nachrichtentext für das Element [' MimeContent '](mimecontent.md) . 
    
3. XML-Dokument – ist dies stets die base64-codierten ASCII-Stream des MIME-Streams, in dem Zeichen wie '\<', welche zu XML, benötigt werden, werden aus XML-Parser ausgeblendet.
    
Jede Ebene ist unabhängig von der Ebene, die er vorangestellt ist.
  
Das **MimeContentUTF8** -Element kann die gleichen Daten enthalten, die anderen Eigenschaften, die mit einem Element zurückgegeben werden enthalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
### <a name="version-differences"></a>Versionsunterschiede

Dieses Element ist in Versionen von Exchange, beginnend mit Build 15.00.0986.00 verfügbar.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

