---
title: Abonnement-GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f86c178-2311-4844-82db-c2a0e469d116
description: Das Subscription-ID-Element stellt den Bezeichner für ein Streaming-Abonnement dar.
ms.openlocfilehash: babf02c514e7fe8711f51ac52e425a18f3ab47f7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457998"
---
# <a name="subscriptionid-getstreamingevents"></a>Abonnement-GetStreamingEvents

Das **Subscription** -ID-Element stellt den Bezeichner für ein Streaming-Abonnement dar. 
  
```XML
<SubscriptionId/>
```

 **SubscriptionIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetStreamingEvents](getstreamingevents.md) <br/> |Stellt den Vorgang dar, der von Clients zum Anfordern von Streaming-Benachrichtigungen vom Server verwendet wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert ist eine GUID.
  
## <a name="remarks"></a>Bemerkungen

Die GUID, die die Abonnement-ID darstellt, wird vom Client Zugriffsserver generiert, wenn das Abonnement erstellt wird.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

