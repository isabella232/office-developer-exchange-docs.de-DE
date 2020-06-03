---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: Das AttachmentIds-Element enthält ein Array von Anlagen-IDs.
ms.openlocfilehash: cff1cb5658690fd6dd2c6a7812e1f600a4c80e29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464252"
---
# <a name="attachmentids"></a>AttachmentIds

Das **AttachmentIds** -Element enthält ein Array von Anlagen-IDs. 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 **NonEmptyArrayOfRequestAttachmentIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Attachment-Nr (GetAttachment und DeleteAttachment-)](attachmentid-getattachment-and-deleteattachment.md) <br/> |Das-Element, das eine einzelne Anlage identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteAttachment-](deleteattachment.md) <br/> |Das-Element, das eine Anforderung zum Löschen einer Anlage aus dem Exchange-Informationsspeicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |Das-Element, das eine Anforderung zum Abrufen einer Anlage aus dem Exchange-Informationsspeicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteAttachment-Vorgang](deleteattachment-operation.md)
- [GetAttachment-Vorgang](getattachment-operation.md)

