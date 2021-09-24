---
title: RootItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RootItemId
api_type:
- schema
ms.assetid: f613c705-17ce-48ce-aa64-4dc2cea25e31
description: Das RootItemId-Element identifiziert das Stammelement einer gelöschten Anlage.
ms.openlocfilehash: eab3cc30c2e3f2b6cdc443ba8eb7ae4bfa38d257
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509368"
---
# <a name="rootitemid"></a>RootItemId

Das **RootItemId-Element** identifiziert das Stammelement einer gelöschten Anlage. 
  
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
|**RootItemId** <br/> |Identifiziert das Stammelement einer gelöschten Anlage.  <br/> |
|**RootItemChangeKey** <br/> |Identifiziert den neuen Änderungsschlüssel des Stammelements einer gelöschten Anlage.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer DeleteAttachment-Anforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **RootItemId-Element** wird nur in DeleteAttachment-Antworten verwendet. Dadurch wird der Stammelementbezeichner und vor allem der neue Änderungsschlüssel für das übergeordnete Element identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[DeleteAttachment](deleteattachment.md)
  
[DeleteAttachment-Vorgang](deleteattachment-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

