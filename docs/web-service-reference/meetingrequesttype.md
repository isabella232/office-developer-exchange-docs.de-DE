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
description: Das MeetingRequestType-Element beschreibt die Art der Besprechungsanfrage.
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830432"
---
# <a name="meetingrequesttype"></a>MeetingRequestType

Das **MeetingRequestType** -Element beschreibt die Art der Besprechungsanfrage. 
  
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

Ein Textwert ist erforderlich. Die folgende Tabelle enthält die möglichen Textwerte für dieses Element.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|FullUpdate  <br/> |Die Besprechungsanfrage identifiziert als eine vollständige Aktualisierung auf eine vorhandene Anforderung. Eine vollständige Aktualisierung wurde aktualisiert, Zeit und informative Inhalte aufweisen.  <br/> |
|InformationalUpdate  <br/> |Identifiziert die Besprechungsanfrage als informative Inhalte aufweisen, enthält, die aktualisiert werden.  <br/> |
|NewMeetingRequest  <br/> |Identifiziert die Besprechungsanfrage als eine neue Besprechungsanfrage.  <br/> |
|Keine  <br/> |Gibt an, dass die Besprechungsanfrage Typ nicht definiert ist.  <br/> |
|Veraltet  <br/> |Die Besprechungsanfrage als veraltet identifiziert.  <br/> |
|PrincipalWantsCopy  <br/> |Gibt an, dass die Besprechungsanfrage zu einem Prinzipal gehört, die Besprechungsnachrichten an die Stellvertretung weitergeleitet und seinen Kopien wie Informationszwecken gekennzeichnet hat.  <br/> |
|SilentUpdate  <br/> |Die Besprechungsanfrage identifiziert als eine automatische Aktualisierung einer vorhandenen Besprechung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

