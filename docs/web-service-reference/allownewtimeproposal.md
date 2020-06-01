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
description: Das AllowNewTimeProposal-Element gibt an, ob eine neue Besprechungszeit für eine Besprechung von einem Teilnehmer vorgeschlagen werden kann.
ms.openlocfilehash: b3f2c569bced08c66144680a4fddd6e8bac0cecf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464805"
---
# <a name="allownewtimeproposal"></a>AllowNewTimeProposal

Das **AllowNewTimeProposal** -Element gibt an, ob eine neue Besprechungszeit für eine Besprechung von einem Teilnehmer vorgeschlagen werden kann. 
  
```xml
<AllowNewTimeProposal/>
```

 **Boolescher Wert**
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

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **true** gibt an, dass ein neuer Vorschlag für die Besprechungszeit erstellt werden kann. der Wert **false** gibt an, dass keine neuen Zeit Vorschläge zulässig sind. Der Organisator legt diesen Wert in der Besprechungsanfrage fest. 
  
## <a name="remarks"></a>Bemerkungen

Die AllowNewTimeProposal-Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt. Er ist schreibgeschützt für Besprechungsanfragen und für die Kalenderelemente von Teilnehmern.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
> [!NOTE]
> Exchange Webdienste unterstützt keine neuen Zeit Angebots Meldungen. Zum Abrufen von Eigenschaften, die sich auf neue Zeit Vorschlags Meldungen beziehen, verwenden Sie erweiterte Eigenschaften. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

