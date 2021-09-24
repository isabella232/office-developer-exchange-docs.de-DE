---
title: AttachmentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttachmentId
api_type:
- schema
ms.assetid: 55a5fd77-60d1-40fa-8144-770600cedc6a
description: Das AttachmentId-Element identifiziert ein Element oder eine Dateianlage. Dieses Element wird in CreateAttachment-Antworten verwendet.
ms.openlocfilehash: a6363fad4e7ef9f0c21377f2c1ea8c19c494cdef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522019"
---
# <a name="attachmentid"></a>AttachmentId

Das **AttachmentId-Element** identifiziert ein Element oder eine Dateianlage. Dieses Element wird in CreateAttachment-Antworten verwendet. 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Identifiziert den eindeutigen Bezeichner der Anlage.  <br/> |
|**RootItemId** <br/> |Gibt den eindeutigen Bezeichner des Stammspeicherelements an, an das die Anlage angefügt ist.  <br/> |
|**RootItemChangeKey** <br/> |Gibt den Änderungsschlüssel des Stammspeicherelements an, an das die Anlage angefügt ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Stellt eine Datei dar, die an ein Element im Exchange Speicher angefügt ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es ist wichtig zu beachten, dass beim Erstellen einer Anlage der Änderungsschlüssel des Stammelements geändert wird.
  
Das [AttachmentId-Element (GetAttachment und DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md) wird in DeleteAttachment- und GetAttachment-Anforderungen verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

