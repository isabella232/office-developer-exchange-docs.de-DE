---
title: RecipientTrackingEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecipientTrackingEvent
api_type:
- schema
ms.assetid: 2bffdac7-c2f5-4805-ae7e-bd865301acb6
description: Das RecipientTrackingEvent-Element enthält Informationen für ein einzelnes Ereignis für einen Empfänger.
ms.openlocfilehash: 30d9cd4ca075fda9607b191f576cac1b7a529988
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525763"
---
# <a name="recipienttrackingevent"></a>RecipientTrackingEvent

Das **RecipientTrackingEvent-Element** enthält Informationen für ein einzelnes Ereignis für einen Empfänger. 
  
```XML
<RecipientTrackingEvent>
   <Date/>
   <Recipient/>
   <DeliveryStatus/>
   <EventDescription/>
   <EventData/>
   <Server/>
   <InternalId/>
   <BccRecipient/>
   <HiddenRecipient/>
   <UniquePathId/>
   <RootAddress/>
   <Properties/>
</RecipientTrackingEvent>
```

 **RecipientTrackingEventType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Datum (MessageTracking)](date-messagetracking.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[Empfänger](recipient.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[DeliveryStatus](deliverystatus.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[EventDescription](eventdescription.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[EventData](eventdata.md) <br/> |Dieses Element ist optional.  <br/> |
|[Server (MessageTracking)](server-messagetracking.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[InternalId](internalid.md) <br/> |Dieses Element ist erforderlich.  <br/> |
|[BccRecipient](bccrecipient.md) <br/> |Dieses Element ist optional.  <br/> |
|[HiddenRecipient](hiddenrecipient.md) <br/> |Dieses Element ist optional.  <br/> |
|[UniquePathId](uniquepathid.md) <br/> |Dieses Element ist optional.  <br/> |
|[RootAddress](rootaddress.md) <br/> |Dieses Element ist optional.  <br/> |
|[Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md) <br/> |Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RecipientTrackingEvents](recipienttrackingevents.md) <br/> |Enthält eine Liste mit einem oder mehreren Nachverfolgungsereignissen für einen Empfänger.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

