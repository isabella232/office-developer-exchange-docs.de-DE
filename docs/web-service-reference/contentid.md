---
title: ContentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContentId
api_type:
- schema
ms.assetid: bc59100d-6079-414b-a6e0-7c15feaa3184
description: Das Content-ID-Element stellt einen Bezeichner für den Inhalt einer Anlage dar. Die Inhalts-Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können mithilfe von Content-ID eigene Identifikations Mechanismen implementieren.
ms.openlocfilehash: ca89c8790e839326412003f26b738ad1ee956211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529266"
---
# <a name="contentid"></a>ContentId

Das **Content** -ID-Element stellt einen Bezeichner für den Inhalt einer Anlage dar. Die **Inhalts** -Nr kann auf einen beliebigen Zeichenfolgenwert festgelegt werden. Anwendungen können mithilfe von **Content** -ID eigene Identifikations Mechanismen implementieren. 
  
```xml
<ContentId/>
```

 **String**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Stellt eine Datei dar, die an ein Element im Exchange-Informationsspeicher angefügt ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der String-Wert stellt den Bezeichner für den Inhalt einer Anlage dar.
  
## <a name="remarks"></a>Bemerkungen

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

