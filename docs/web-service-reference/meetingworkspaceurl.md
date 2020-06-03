---
title: MeetingWorkspaceUrl
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingWorkspaceUrl
api_type:
- schema
ms.assetid: 0ca942fe-8f57-4065-93ad-65790f9a04c3
description: Das MeetingWorkspaceUrl-Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist. Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen der Besprechung und zum Nachverfolgen der Ergebnisse.
ms.openlocfilehash: cd4396e590ab1471278bd44b9a4e0009fe326eaf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466283"
---
# <a name="meetingworkspaceurl"></a>MeetingWorkspaceUrl

Das **MeetingWorkspaceUrl** -Element enthält die URL für den Besprechungsarbeitsbereich, der im Kalenderelement enthalten ist. Ein Besprechungsarbeitsbereich ist eine freigegebene Website zum Planen der Besprechung und zum Nachverfolgen der Ergebnisse. 
  
```xml
<MeetingWorkspaceUrl/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Text Wert, der eine URL darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Bemerkungen

Die MeetingWorkspaceUrl-Eigenschaft ist für das Kalenderelement des Organisators schreibgeschützt. Er ist schreibgeschützt für Besprechungsanfragen und für die Kalenderelemente von Teilnehmern.
  
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

