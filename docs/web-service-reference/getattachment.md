---
title: GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 9443cf96-b451-4530-b868-490dff798673
description: Das GetAttachment-Element ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange-Informationsspeicher.
ms.openlocfilehash: d03d086ff443db87b0104a2ec83599eb9eaea6b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463979"
---
# <a name="getattachment"></a>GetAttachment

Das **GetAttachment** -Element ist das Stammelement in einer Anforderung zum Abrufen einer Anlage aus dem Exchange-Informationsspeicher. 
  
```xml
<GetAttachment>
   <AttachmentShape/>
   <AttachmentIds/>
</GetAttachment>
```

 **Getattachmenttype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> |Identifiziert zusätzliche erweiterte Elementeigenschaften, die in einer Antwort auf eine [GetAttachment](getattachment.md) -Anforderung zurückgegeben werden sollen. Dieses Element ist optional.  <br/> |
|[AttachmentIds](attachmentids.md) <br/> |Enthält ein Array von Anlagen Bezeichnern.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das [AttachmentShape](attachmentshape.md) -Element ist nicht erforderlich, um die Eigenschaften zu identifizieren, die in der Antwort zurückgegeben werden. Der [GetAttachment-Vorgang](getattachment-operation.md) gibt den Namen, den ContentType, die Inhalts-ContentLocation und die Inhaltseigenschaften für Dateianlagen zurück. Bei Element Anlagen sind die zurückgegebenen Eigenschaften der Name, der ContentType, die Inhalts-ContentLocation und alle Eigenschaften des angefügten Elements. Dies entspricht der Verwendung des allproperties-Basis-Shapes in einer [GetItem](getitem.md) -Anforderung. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetAttachment-Vorgang](getattachment-operation.md)
  
[GetAttachmentResponse](getattachmentresponse.md)

