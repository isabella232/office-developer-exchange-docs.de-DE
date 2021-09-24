---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: Das MeetingRequestType-Element beschreibt den Typ der Besprechungsanfrage.
ms.openlocfilehash: 1a8371331691bb9dee5595b0130ec0c3c75c47c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539374"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

Das **MeetingRequestType-Element** beschreibt den Typ der Besprechungsanfrage. 
  
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

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Textwerte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|FullUpdate  <br/> |Identifiziert die Besprechungsanfrage als vollständige Aktualisierung einer vorhandenen Anforderung. Ein vollständiges Update hat zeit- und informationsbezogene Inhalte aktualisiert.  <br/> |
|InformationalUpdate  <br/> |Identifiziert die Besprechungsanfrage als nur mit aktualisierten Informationsinhalten.  <br/> |
|NewMeetingRequest  <br/> |Identifiziert die Besprechungsanfrage als neue Besprechungsanfrage.  <br/> |
|Keines  <br/> |Gibt an, dass der Besprechungsanfragetyp nicht definiert ist.  <br/> |
|Veraltet  <br/> |Identifiziert die Besprechungsanfrage als veraltet.  <br/> |
|PrincipalWantsCopy  <br/> |Gibt an, dass die Besprechungsanfrage zu einem Prinzipal gehört, der Besprechungsnachrichten an eine Stellvertretung weitergeleitet hat und seine Kopien als informativ markiert hat.  <br/> |
|SilentUpdate  <br/> |Identifiziert die Besprechungsanfrage als automatische Aktualisierung einer vorhandenen Besprechung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

