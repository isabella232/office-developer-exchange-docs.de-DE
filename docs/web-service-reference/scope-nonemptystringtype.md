---
title: Bereich (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Scope
api_type:
- schema
ms.assetid: 7efb6fd9-1615-469e-96f6-0f7846ad9b44
description: Das Bereich-Element gibt den Bereich der Bericht mit der Verfolgung an.
ms.openlocfilehash: 534ed23916a60b246c7cb5be4a59d086980a7c37
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831280"
---
# <a name="scope-nonemptystringtype"></a>Bereich (NonEmptyStringType)

Das **Bereich** -Element gibt den Bereich der Bericht mit der Verfolgung an. 
  
```XML
<Scope>Organization | Forest | Site</Scope>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindMessageTrackingReport](findmessagetrackingreport.md) | [GetMessageTrackingReport](getmessagetrackingreport.md)
  
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das Element **Bereich** . 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Organisation  <br/> |Die nachrichtenverfolgung Bereiche erstreckt sich innerhalb einer Organisation.  <br/> |
|Gesamtstruktur  <br/> |Die nachrichtenverfolgung Bereiche erstreckt sich auf einer Gesamtstruktur.  <br/> |
|Website  <br/> |Die nachrichtenverfolgung Bereiche erstreckt sich auf einer Website.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

