---
title: MimeContentUTF8
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 31544c95-5231-4b57-958c-2a689464d29b
description: Das MimeContentUTF8-Element enthält den UTF-8-MIME-Stream eines Objekts, das im Base64Binary-Format dargestellt wird und die Internationalisierung von E-Mail-Adressen und [RFC6530] unterstützt.
ms.openlocfilehash: f0ab38368d3a18be38f63c86183a238e2fd0a474
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540755"
---
# <a name="mimecontentutf8"></a>MimeContentUTF8

Das **MimeContentUTF8-Element** enthält den UTF-8-MIME-Stream eines Objekts, das im Base64Binary-Format dargestellt wird und die Internationalisierung von E-Mail-Adressen und [[RFC6530]](http://www.rfc-editor.org/rfc/rfc6530.txt)unterstützt.
  
```XML
<MimeContentUTF8 CharacterSet="" />
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

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich, der einen base64binary MIME-Datenstrom darstellt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Nachrichteninhalt durchläuft die folgenden drei Codierungsebenen, bevor er im **MimeContentUTF8-Wert** gespeichert wird: 
  
1. Nachrichtentext – Dies ist die Textcodierung, z. B. iso-2022-jp für japanische Zeichen.
    
2. MIME-Stream – Dies ist die UTF8-Codierung des Nachrichtentexts für das **MimeContentUTF8-Element** oder die ASCII-Codierung des Nachrichtentexts für das [MimeContent-Element.](mimecontent.md) 
    
3. XML-Dokument – Dies ist immer der base64-codierte ASCII-Stream des MIME-Datenstroms, wobei Zeichen wie " \< ", die für XML von Bedeutung sind, vor XML-Parsern ausgeblendet werden.
    
Jede Ebene ist unabhängig von der Ebene, die ihr vorausgeht.
  
Das **MimeContentUTF8-Element** kann dieselben Daten enthalten wie andere Eigenschaften, die mit einem Element zurückgegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
### <a name="version-differences"></a>Versionsunterschiede

Dieses Element ist in Versionen von Exchange ab Build 15.00.0986.00 verfügbar.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

