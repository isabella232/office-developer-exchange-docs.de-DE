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
description: Das Element FileAttachment repräsentiert eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.
ms.openlocfilehash: 5ce7aef753313aa9430f640bb3c26f652b8c1c43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758426"
---
# <a name="fileattachment"></a>FileAttachment

Das Element **FileAttachment** repräsentiert eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist. 
  
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

 **FileAttachmentType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentId](attachmentid.md) <br/> |Identifiziert die Dateianlage.  <br/> |
|[Name ("AttachmentType")](name-attachmenttype.md) <br/> |Stellt den Namen der Anlage an.  <br/> |
|[ContentType](contenttype.md) <br/> |Beschreibt den Multipurpose Internet Mail Extensions (MIME) gescannt.  <br/> |
|[ContentId](contentid.md) <br/> |Stellt einen Bezeichner für den Inhalt einer Anlage an. [ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können [ContentId](contentid.md) um eigene Kennung Mechanismen zu implementieren.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Enthält den URI Uniform Resource Identifier (), die den Speicherort des Inhalts der Anlage entspricht.  <br/> |
|[Size](size.md) <br/> |Stellt die Größe des Dateianlage in Bytes.  <br/> |
|[ZuletztGeändertUm](lastmodifiedtime.md) <br/> |Stellt die bei die Dateianlage zuletzt geändert wurde.  <br/> |
|[IsInline](isinline.md) <br/> |Stellt dar, ob die Anlage Inline innerhalb eines Elements angezeigt wird.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Gibt an, ob die Dateianlage ein Kontaktbild ist.  <br/> |
|[Inhalt](content.md) <br/> |Enthält den Base64-codierten Inhalt der Dateianlage.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

