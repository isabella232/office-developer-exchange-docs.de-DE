---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: Das Element AttachmentId identifiziert eine Anlage Element oder eine Datei. Dieses Element wird in CreateAttachment Antworten verwendet.
ms.openlocfilehash: 2910503d1661ca3aaeeb4e319deb39f6b57c5c0a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757393"
---
# <a name="attachmentid"></a>AttachmentId

Das Element **AttachmentId** identifiziert eine Anlage Element oder eine Datei. Dieses Element wird in CreateAttachment Antworten verwendet. 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Gibt die eindeutige ID der Anlage an.  <br/> |
|**RootItemId** <br/> |Gibt den eindeutigen Bezeichner des Elements Stamm-Speicher, dem die Anlage angefügt werden.  <br/> |
|**RootItemChangeKey** <br/> |Identifiziert die Key ändern des Elements Stamm-Speicher, dem die Anlage angefügt werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Stellt eine Datei, die ein Element in der Exchange-Informationsspeicher zugeordnet ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Es ist wichtig, beachten Sie, dass wenn eine Anlage erstellt wird, der Key ändern die Stamm-Elements geändert wird.
  
Das Element [AttachmentId (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) wird in DeleteAttachment und GetAttachment Anforderungen verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

