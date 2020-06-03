---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: Das MeetingRequestType-Element beschreibt den Typ der Besprechungsanfrage.
ms.openlocfilehash: e90c44dd4124d698ca5ef7655f6429a7167673e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465786"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

Das **MeetingRequestType** -Element beschreibt den Typ der Besprechungsanfrage. 
  
```xml
<MeetingRequestType/>
```

 **MeetingRequestTypeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Text Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|FullUpdate  <br/> |Identifiziert die Besprechungsanfrage als vollständige Aktualisierung einer vorhandenen Anforderung. Eine vollständige Aktualisierung enthält aktualisierte Zeit-und Informationsinhalte.  <br/> |
|InformationalUpdate  <br/> |Identifiziert die Besprechungsanfrage als nur mit aktualisierten Informationsinhalten.  <br/> |
|NewMeetingRequest  <br/> |Identifiziert die Besprechungsanfrage als neue Besprechungsanfrage.  <br/> |
|Keine  <br/> |Gibt an, dass der Typ der Besprechungsanfrage nicht definiert ist.  <br/> |
|Veraltete  <br/> |Identifiziert die Besprechungsanfrage als veraltet.  <br/> |
|PrincipalWantsCopy  <br/> |Gibt an, dass die Besprechungsanfrage einem Prinzipal gehört, der Besprechungsnachrichten an eine Stellvertretung weitergeleitet hat und seine Kopien als Information markiert hat.  <br/> |
|SilentUpdate  <br/> |Identifiziert die Besprechungsanfrage als eine unbeaufsichtigte Aktualisierung für eine vorhandene Besprechung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

