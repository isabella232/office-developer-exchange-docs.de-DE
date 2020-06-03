---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: Das FileAttachment-Element stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.
ms.openlocfilehash: db9b541fb2527ae3c09cbdb33bedea7fb215bd30
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461016"
---
# <a name="fileattachment"></a>FileAttachment

Das **FileAttachment** -Element stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist. 
  
```XML
<FileAttachment>
   <AttachmentId/>
   <Name/>
   <ContentType/>
   <ContentId/>
   <ContentLocation/>
   <Size/>
   <LastModifiedTime/>
   <IsInline/>
   <IsContactPhoto/>
   <Content/>
</FileAttachment>
```

 **Fileattachmenttype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifiziert die Dateianlage.  <br/> |
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |Stellt den Namen der Anlage dar.  <br/> |
|[ContentType](contenttype.md) <br/> |Beschreibt die Multipurpose Internet Mail Extensions (MIME) Art des Anlage Inhalts.  <br/> |
|[ContentId](contentid.md) <br/> |Stellt einen Bezeichner für den Inhalt einer Anlage dar. Die [Inhalts](contentid.md) -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können mithilfe von [Content](contentid.md) -ID eigene Identifikations Mechanismen implementieren.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe der Dateianlage in Bytes dar.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Stellt dar, wann die Dateianlage zuletzt geändert wurde.  <br/> |
|[IsInline](isinline.md) <br/> |Stellt dar, ob die Anlage Inline in einem Element angezeigt wird.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Gibt an, ob es sich bei der Dateianlage um ein Kontaktbild handelt.  <br/> |
|[Content](content.md) <br/> |Enthält den Base64-codierten Inhalt der Dateianlage.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.  <br/> |
   
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

