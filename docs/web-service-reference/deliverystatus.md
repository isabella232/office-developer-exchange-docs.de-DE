---
title: DeliveryStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeliveryStatus
api_type:
- schema
ms.assetid: eab55db3-affb-42be-a586-5caa04052433
description: Das DeliveryStatus-Element gibt den Status für eine Nachricht an.
ms.openlocfilehash: f11952f401e0d22d780725598bfb32cbd3a8d622
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543387"
---
# <a name="deliverystatus"></a>DeliveryStatus

Das **DeliveryStatus-Element** gibt den Status für eine Nachricht an. 
  
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
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Textwerte für das **DeliveryStatus-Element** aufgeführt. 
  
**DeliveryStatus-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolglos  <br/> |Gibt an, dass eine Nachricht nicht zugestellt wurde.  <br/> |
|Ausstehend  <br/> |Gibt an, dass die Nachricht auf die Genehmigung durch einen Moderator wartet.  <br/> |
|Geliefert  <br/> |Gibt an, dass die Nachricht an alle angegebenen Empfänger übermittelt wurde.  <br/> |
|Übertragen  <br/> |Gibt an, dass die Nachricht an einen Server außerhalb des Suchbereichs übertragen wurde.  <br/> |
|Lesen  <br/> |Gibt an, dass die Nachricht von den Empfängern übermittelt und gelesen wurde.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **DeliveryStatus-Element** war vom Typ **MessageTrackingDeliveryStatusType** in Exchange Server 2010. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

