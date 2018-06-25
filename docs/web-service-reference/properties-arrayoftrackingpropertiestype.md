---
title: Eigenschaften (ArrayOfTrackingPropertiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Properties
api_type:
- schema
ms.assetid: 175566d2-fd62-45a2-8518-2827912cec88
description: Das Properties-Element enthält eine Liste der Eigenschaften für eine oder mehrere Tracking.
ms.openlocfilehash: 079d2d2c101fdeb7f26d65798048c3c6c59f3e94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830897"
---
# <a name="properties-arrayoftrackingpropertiestype"></a>Eigenschaften (ArrayOfTrackingPropertiesType)

Das **Properties** -Element enthält eine Liste der Eigenschaften für eine oder mehrere Tracking. 
  
- [FindMessageTrackingReport](findmessagetrackingreport.md)
  
- [Eigenschaften (ArrayOfTrackingPropertiesType)](properties-arrayoftrackingpropertiestype.md)
  
```xml
<Properties>
   <TrackingPropertyType/>
</Properties>
```

**ArrayOfTrackingPropertiesType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Stellt ein Name-Wert-Paar von Zeichenfolgen, die zum Erstellen von Eigenschaften für nachrichtenverfolgungsberichte verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Gibt Kriterien für die Typen von Nachrichten suchen.  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [FindMessageTrackingReport Vorgang](findmessagetrackingreport-operation.md) .  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Enthält die Anforderung für den [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) zum Abrufen der vollständigen Nachricht Nachverfolgen der Bericht für den angegebenen ID.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Enthält das Ergebnis einer einzelnen Anforderung [GetMessageTrackingReport Vorgang](getmessagetrackingreport-operation.md) .  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen für ein einzelnes Ereignis für einen Empfänger.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Ein einzelnes Nachricht Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)
- [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

