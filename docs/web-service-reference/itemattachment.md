---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: Das ItemAttachment-Element stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist.
ms.openlocfilehash: 09324e8f3cbd149cbe7cbd1a6291a703620e27fb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540882"
---
# <a name="itemattachment"></a>ItemAttachment

Das **ItemAttachment-Element** stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist. 
  
```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Item/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Message/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <CalendarItem/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Contact/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <Task/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingMessage/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingRequest/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingResponse/>
</ItemAttachment>
```

```xml
<ItemAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <MeetingCancellation/>
</ItemAttachment>
```

**ItemAttachmentType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifiziert die Anlage.  <br/> |
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |Stellt den Namen der Anlage dar.  <br/> |
|[ContentType](contenttype.md) <br/> |Beschreibt den MIME-Typ (Multipurpose Internet Mail Extensions) des Anlageninhalts.  <br/> |
|[ContentId](contentid.md) <br/> |Stellt einen Bezeichner für den Inhalt der Anlage dar. [ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können [ContentId](contentid.md) verwenden, um ihre eigenen Identifikationsmechanismen zu implementieren.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe der Dateianlage in Byte dar.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann die Anlage zuletzt geändert wurde.  <br/> |
|[IsInline](isinline.md) <br/> |Gibt an, ob die Anlage inline in einem Element angezeigt wird.  <br/> |
|[Aspekt](item.md) <br/> |Stellt eine generische Exchange Elementanlage dar.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange E-Mail-Nachrichtenanlage dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt eine Exchange Kalenderelementanlage dar.  <br/> |
|[Contact](contact.md) <br/> |Stellt eine Exchange Kontaktelementanlage dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Exchange Vorgangsanlage dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anhänge](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente und/oder Dateien, die an ein Element im Exchange Speicher angefügt sind.  <br/> |
   
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

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

