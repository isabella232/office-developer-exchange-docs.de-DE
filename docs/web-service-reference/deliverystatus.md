---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: Das DeliveryStatus-Element gibt den Status für eine Nachricht an.
ms.openlocfilehash: 4e6f31e8ef4f98d8e838ba91167c7dd5d6ab2590
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757948"
---
# <a name="deliverystatus"></a>DeliveryStatus

Das **DeliveryStatus** -Element gibt den Status für eine Nachricht an. 
  
```XML
<DeliveryStatus>Unsuccessful | Pending | Delivered | Transferred | Read</DeliveryStatus>
```

 **MessageTrackingDeliveryStatusType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Textwerte für das **DeliveryStatus** -Element. 
  
**DeliveryStatus-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Nicht erfolgreich  <br/> |Gibt an, dass eine Nachricht nicht übermittelt wurde.  <br/> |
|Ausstehende  <br/> |Gibt an, dass die Nachricht zur Genehmigung von einen Moderator wartet.  <br/> |
|Übermittelt  <br/> |Gibt an, dass die Nachricht an alle der angegebenen Empfänger gesendet wurde.  <br/> |
|Übertragen  <br/> |Gibt an, dass die Nachricht an einen Server außerhalb der Suchbereich übertragen wurde.  <br/> |
|Lesen  <br/> |Gibt an, dass die Nachricht übermittelt und vom Empfänger gelesen wurde.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **DeliveryStatus** -Element wurde vom Typ **MessageTrackingDeliveryStatusType** in Exchange Server 2010. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

