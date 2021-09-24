---
title: AttachmentIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: Das AttachmentIds-Element enthält ein Array von Anlagenbezeichnern.
ms.openlocfilehash: a631edbd1b82f3bbf7b99014d623fbb0072bb0c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525134"
---
# <a name="attachmentids"></a>AttachmentIds

Das **AttachmentIds-Element** enthält ein Array von Anlagenbezeichnern. 
  
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
|[AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) <br/> |Das Element, das eine einzelne Anlage identifiziert.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteAttachment](deleteattachment.md) <br/> |Das Element, das eine Anforderung zum Löschen einer Anlage aus dem Exchange Speicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/DeleteAttachment` <br/> |
|[GetAttachment](getattachment.md) <br/> |Das Element, das eine Anforderung zum Abrufen einer Anlage aus dem Exchange Speicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteAttachment-Vorgang](deleteattachment-operation.md)
- [GetAttachment-Vorgang](getattachment-operation.md)

