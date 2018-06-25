---
title: ErrorSubscriptionIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ErrorSubscriptionIds
api_type:
- schema
ms.assetid: e64e76ff-4d98-4082-9acc-a1114ae45f44
description: Das ErrorSubscriptionIds-Element enthält ein Array von Ungültiges Abonnement IDs.
ms.openlocfilehash: 5cdbbeb1083754510f431bc092bb67dc0addecab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758276"
---
# <a name="errorsubscriptionids"></a>ErrorSubscriptionIds

Das **ErrorSubscriptionIds** -Element enthält ein Array von Ungültiges Abonnement IDs. 
  
```xml
<ErrorSubscriptionIds>
   <SubscriptionId/>
</ErrorSubscriptionIds>
```

 **NonEmptyArrayOfSubscriptionIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |Stellt den Bezeichner für ein Abonnement.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetStreamingEventsResponseMessage](getstreamingeventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [GetStreamingEvents Vorgang](getstreamingevents-operation.md) .  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages und http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema Typen-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd; Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

