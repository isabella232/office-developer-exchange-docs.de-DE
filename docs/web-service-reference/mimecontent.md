---
title: MimeContent
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MimeContent
api_type:
- schema
ms.assetid: 4f472a08-5653-4c54-ba65-831dfe32f20f
description: Das MimeContent-Element enthält den ASCII-MIME-Strom eines Objekts, das im base64Binary-Format dargestellt wird und [RFC2045] unterstützt.
ms.openlocfilehash: 43040f241008010620ff4f1018cc5410a7a00e42
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542071"
---
# <a name="mimecontent"></a>MimeContent

Das **MimeContent-Element** enthält den ASCII-MIME-Strom eines Objekts, das im Base64Binary-Format dargestellt wird und [[RFC2045]](http://www.rfc-editor.org/rfc/rfc2045.txt)unterstützt.
  
```xml
<MimeContent CharacterSet="" />
```

 **MimeContentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Characterset** <br/> |Wenn dieser Wert festgelegt ist, wird der Wert für dieses Attribut vom Server ignoriert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[CalendarItem](calendaritem.md)  |  [Kontakt](contact.md)  |  [DistributionList](distributionlist.md)  |  [Element](item.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [RemoveItem](removeitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich, der einen base64Binary-MIME-Datenstrom darstellt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichteninhalt durchläuft die folgenden drei Codierungsebenen, bevor er im **MimeContent-Wert** gespeichert wird: 
  
1. Nachrichtentext – Dies ist die Textcodierung, z. B. iso-2022-jp für japanische Zeichen.
    
2. MIME-Datenstrom – Dies ist die ASCII-Codierung des Nachrichtentexts für das **MimeContent-Element** oder die UTF8-Codierung des Nachrichtentexts für das [MimeContentUTF8-Element.](mimecontentutf8.md) 
    
3. XML-Dokument – Dies ist immer der base64-codierte ASCII-Stream des MIME-Datenstroms, wobei Zeichen wie " \< ", die für XML von Bedeutung sind, vor XML-Parsern ausgeblendet werden.
    
Jede Ebene ist unabhängig von der Ebene, die ihr vorausgeht.
  
Das **MimeContent-Element** kann dieselben Daten enthalten, die auch andere Eigenschaften enthalten, die mit einem Element zurückgegeben werden. 
  
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

