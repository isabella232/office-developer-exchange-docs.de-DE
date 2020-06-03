---
title: ItemAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemAttachment
api_type:
- schema
ms.assetid: 089ee599-f45e-46f5-a18a-5cfb3d2851ff
description: Das ItemAttachment-Element stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.
ms.openlocfilehash: c3a07fa091c05654a03cbff58fb20204c26c9061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526438"
---
# <a name="itemattachment"></a>ItemAttachment

Das **ItemAttachment** -Element stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist. 
  
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
|[ContentType](contenttype.md) <br/> |Beschreibt die Multipurpose Internet Mail Extensions (MIME) Art des Anlage Inhalts.  <br/> |
|[ContentId](contentid.md) <br/> |Stellt einen Bezeichner für den Inhalt der Anlage dar. Die [Inhalts](contentid.md) -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können mithilfe von [Content](contentid.md) -ID eigene Identifikations Mechanismen implementieren.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe der Dateianlage in Bytes dar.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Stellt dar, wann die Anlage zuletzt geändert wurde.  <br/> |
|[IsInline](isinline.md) <br/> |Stellt dar, ob die Anlage Inline in einem Element angezeigt wird.  <br/> |
|[Element](item.md) <br/> |Stellt eine generische Exchange-Elementanlage dar.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-e-Mail-Nachrichtenanlage dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt eine Exchange-Kalenderelement Anlage dar.  <br/> |
|[Contact](contact.md) <br/> |Stellt eine Exchange-Kontaktelement Anlage dar.  <br/> |
|[Task](task.md) <br/> |Stellt eine Exchange-Aufgabenanlage dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente und/oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

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

