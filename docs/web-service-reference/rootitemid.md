---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: Das RootItemId-Element identifiziert das Stammelement der Anlage zu einer gelöschten.
ms.openlocfilehash: 484b185db63c9692eaca7e43c49d6e95375a1a98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831251"
---
# <a name="rootitemid"></a>RootItemId

Das **RootItemId** -Element identifiziert das Stammelement der Anlage zu einer gelöschten. 
  
[DeleteAttachmentResponse](deleteattachmentresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
  
[RootItemId](rootitemid.md)
  
```xml
<RootItemId RootItemId="" RootItemChangeKey="" />
```

 **RootItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**RootItemId** <br/> |Das Stammelement der Anlage zu einer gelöschten identifiziert.  <br/> |
|**RootItemChangeKey** <br/> |Gibt den neuen Änderungsschlüssel des Elements Stamm einer gelöschten Anlage.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung DeleteAttachment.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Element **RootItemId** wird nur in DeleteAttachment Antworten verwendet. Der Elementbezeichner Stamm und darüber hinaus die neue Key ändern, die dem übergeordneten Element identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[DeleteAttachment](deleteattachment.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

