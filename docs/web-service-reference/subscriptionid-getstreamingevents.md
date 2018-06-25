---
title: SubscriptionId (GetStreamingEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f86c178-2311-4844-82db-c2a0e469d116
description: Das Element SubscriptionId stellt den Bezeichner für ein Abonnement streaming.
ms.openlocfilehash: eb451e611c4922fa3b9cff7edec54dfb8260f5f5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839130"
---
# <a name="subscriptionid-getstreamingevents"></a>SubscriptionId (GetStreamingEvents)

Das Element **SubscriptionId** stellt den Bezeichner für ein Abonnement streaming. 
  
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
|[GetStreamingEvents](getstreamingevents.md) <br/> |Stellt die Operation, die von Clients zum Anfordern von streaming Benachrichtigungen vom Server verwendet wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert ist eine GUID.
  
## <a name="remarks"></a>Hinweise

Die GUID, die die Abonnement-ID darstellt wird vom Client Access Server generiert, wenn das Abonnement erstellt wird.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

