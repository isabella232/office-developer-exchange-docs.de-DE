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
description: Das Attachments-Element identifiziert ein Element oder eine Dateianlage. Dieses Element wird in CreateAttachment-Antworten verwendet.
ms.openlocfilehash: b5dc9299b615f0fc01b8afcbaabf0ec7996e53d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459111"
---
# <a name="attachmentid"></a>AttachmentId

Das **Attachments** -Element identifiziert ein Element oder eine Dateianlage. Dieses Element wird in CreateAttachment-Antworten verwendet. 
  
```xml
<AttachmentId Id="" RootItemId="" RootItemChangeKey="" />
```

 **AttachmentIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Gibt den eindeutigen Bezeichner der Anlage an.  <br/> |
|**RootItemId** <br/> |Gibt den eindeutigen Bezeichner des Stammspeicher Elements an, an das die Anlage angefügt ist.  <br/> |
|**RootItemChangeKey** <br/> |Gibt den Änderungsschlüssel des Stammspeicher Elements an, an das die Anlage angefügt ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Es ist wichtig zu beachten, dass beim Erstellen einer Anlage der Änderungsschlüssel des Stammelements geändert wird.
  
Das [Attachment-Element (GetAttachment und DeleteAttachment-)](attachmentid-getattachment-and-deleteattachment.md) wird in DeleteAttachment--und GetAttachment-Anforderungen verwendet. 
  
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

