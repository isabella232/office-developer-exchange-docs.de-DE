---
title: AllowNewTimeProposal
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AllowNewTimeProposal
api_type:
- schema
ms.assetid: afdb4ec9-2daf-48a1-a0bb-a7f647f212f2
description: Das AllowNewTimeProposal-Element gibt an, ob ein Teilnehmer eine neue Besprechungszeit für eine Besprechung vorschlagen kann.
ms.openlocfilehash: 1acb95189e1949204a25f97a82770b88590df776
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543730"
---
# <a name="allownewtimeproposal"></a>AllowNewTimeProposal

Das **AllowNewTimeProposal-Element** gibt an, ob ein Teilnehmer eine neue Besprechungszeit für eine Besprechung vorschlagen kann. 
  
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

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **"true"** gibt an, dass ein neuer Vorschlag für die Besprechungszeit erstellt werden kann. Der Wert **"false"** gibt an, dass neue Zeitvorschläge nicht zulässig sind. Der Organisator legt diesen Wert in der Besprechungsanfrage fest. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die AllowNewTimeProposal-Eigenschaft kann für das Kalenderelement des Organisators schreibgeschützt werden. Sie ist schreibgeschützt für Besprechungsanfragen und die Kalenderelemente der Teilnehmer.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
> [!NOTE]
> Exchange Webdienste unterstützen keine neuen Zeitvorschlagsmeldungen. Verwenden Sie erweiterte Eigenschaften, um Eigenschaften abzurufen, die sich auf neue Zeitvorschlagsnachrichten beziehen. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

