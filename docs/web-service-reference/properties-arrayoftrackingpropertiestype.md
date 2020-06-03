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
description: Das properties-Element enthält eine Liste mit einer oder mehreren Überwachungseigenschaften.
ms.openlocfilehash: 007a4dc14c84c47ea7af8ccacc554c134d563e44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465632"
---
# <a name="properties-arrayoftrackingpropertiestype"></a>Eigenschaften (ArrayOfTrackingPropertiesType)

Das **Properties** -Element enthält eine Liste mit einer oder mehreren Überwachungseigenschaften. 
  
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
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Stellt ein Name-Wert-Paar von Zeichenfolgen dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Gibt Kriterien für die Typen von Nachrichten an, die gesucht werden sollen.  <br/> |
|[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [FindMessageTrackingReport-Vorgangs](findmessagetrackingreport-operation.md) Anforderung.  <br/> |
|[GetMessageTrackingReport](getmessagetrackingreport.md) <br/> |Enthält die Anforderung für den [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md) zum Abrufen des vollständigen Nachrichtenverfolgungsberichts für die angegebene ID.  <br/> |
|[GetMessageTrackingReportResponse](getmessagetrackingreportresponse.md) <br/> |Enthält das Ergebnis einer einzelnen [GetMessageTrackingReport-Vorgangs](getmessagetrackingreport-operation.md) Anforderung.  <br/> |
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Enthält Informationen zu einem einzelnen Ereignis für einen Empfänger.  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Enthält eine Nachricht, die in einem [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)zurückgegeben wird.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Enthält ein einzelnes Nachrichten Ergebnis für ein [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) -Element.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindMessageTrackingReport-Vorgang](findmessagetrackingreport-operation.md)
- [GetMessageTrackingReport-Vorgang](getmessagetrackingreport-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

