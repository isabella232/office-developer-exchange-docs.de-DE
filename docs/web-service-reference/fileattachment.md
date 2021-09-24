---
title: FileAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FileAttachment
api_type:
- schema
ms.assetid: 3ecea174-73d1-47fd-8917-6065cef1d565
description: Das FileAttachment-Element stellt eine Datei dar, die an ein Element im Exchange Speicher angefügt ist.
ms.openlocfilehash: 66424fefafd2084bf0b6f45881089448593e621d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518498"
---
# <a name="fileattachment"></a>FileAttachment

Das **FileAttachment-Element** stellt eine Datei dar, die an ein Element im Exchange Speicher angefügt ist. 
  
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
|[Name (AttachmentType)](name-attachmenttype.md) <br/> |Stellt den Namen der Anlage dar.  <br/> |
|[ContentType](contenttype.md) <br/> |Beschreibt den MIME-Typ (Multipurpose Internet Mail Extensions) des Anlageninhalts.  <br/> |
|[ContentId](contentid.md) <br/> |Stellt einen Bezeichner für den Inhalt einer Anlage dar. [ContentId](contentid.md) kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können [ContentId](contentid.md) verwenden, um ihre eigenen Identifikationsmechanismen zu implementieren.  <br/> |
|[ContentLocation](contentlocation.md) <br/> |Enthält den URI (Uniform Resource Identifier), der dem Speicherort des Inhalts der Anlage entspricht.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe der Dateianlage in Byte dar.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann die Dateianlage zuletzt geändert wurde.  <br/> |
|[IsInline](isinline.md) <br/> |Gibt an, ob die Anlage inline in einem Element angezeigt wird.  <br/> |
|[IsContactPhoto](iscontactphoto.md) <br/> |Gibt an, ob es sich bei der Dateianlage um ein Kontaktbild handelt.  <br/> |
|[Inhalt](content.md) <br/> |Enthält den Base64-codierten Inhalt der Dateianlage.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anhänge](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange Speicher angefügt sind.  <br/> |
   
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

