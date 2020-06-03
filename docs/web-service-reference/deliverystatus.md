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
description: Das DeliveryStatus-Element gibt den Status einer Nachricht an.
ms.openlocfilehash: ae32202284d3dd272f693fbb7b76070cb6019d28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461401"
---
# <a name="deliverystatus"></a>DeliveryStatus

Das **DeliveryStatus** -Element gibt den Status einer Nachricht an. 
  
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

In der folgenden Tabelle sind die möglichen Text Werte für das **DeliveryStatus** -Element aufgeführt. 
  
**DeliveryStatus-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Erfolglos  <br/> |Gibt an, dass eine Nachricht nicht zugestellt wurde.  <br/> |
|Ausstehend  <br/> |Gibt an, dass die Nachricht von einem Moderator auf die Genehmigung wartet.  <br/> |
|Geliefert  <br/> |Gibt an, dass die Nachricht an alle angegebenen Empfänger übermittelt wurde.  <br/> |
|Übertragenen  <br/> |Gibt an, dass die Nachricht an einen Server außerhalb des Suchbereichs übertragen wurde.  <br/> |
|Read  <br/> |Gibt an, dass die Nachricht von den Empfängern zugestellt und gelesen wurde.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **DeliveryStatus** -Element war vom Typ **MessageTrackingDeliveryStatusType** in Exchange Server 2010. 
  
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

