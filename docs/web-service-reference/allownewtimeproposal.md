---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: Das AllowNewTimeProposal-Element gibt an, ob für eine Besprechung durch ein Teilnehmer eine neue Besprechungszeit vorgeschlagen werden kann.
ms.openlocfilehash: d5deed5044769c477ffe54cc533d5261ba2e1932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757253"
---
# <a name="allownewtimeproposal"></a>AllowNewTimeProposal

Das **AllowNewTimeProposal** -Element gibt an, ob für eine Besprechung durch ein Teilnehmer eine neue Besprechungszeit vorgeschlagen werden kann. 
  
```xml
<AllowNewTimeProposal/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **true** gibt an, dass für die Besprechungszeit ein neues Vorschlags erstellt werden kann; der Wert **false** gibt an, dass neue Zeit Vorschläge nicht zulässig sind. Der Organisator Festlegen dieses Werts in der Besprechungsanfrage. 
  
## <a name="remarks"></a>Hinweise

Die AllowNewTimeProposal-Eigenschaft kann für den Organisator Kalenderelement lesen geschrieben werden. Es ist schreibgeschützt, für Besprechungsanfragen und Kalenderelemente Teilnehmer.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
> [!NOTE]
> Exchange-Webdienste unterstützt keine neue Zeit Vorschlag Nachrichten. Um die Eigenschaften, die im Zusammenhang mit neuen Uhrzeit Vorschlag Nachrichten erhalten möchten, verwenden Sie erweiterte Eigenschaften. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

