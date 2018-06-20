---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: Das SuggestionsViewOptions-Element enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.
ms.openlocfilehash: 09ff317ae0b2ebf1eadc89dc3bb1cf5b3ae19dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839139"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

Das **SuggestionsViewOptions** -Element enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
```xml
<SuggestionsViewOptions>
   <GoodThreshold>...</GoodThreshold>
   <MaximumResultsByDay>...</MaximumResultsByDay>
   <MaximumNonWorkingHourResultsByDay>...</MaximumNonWorkingHourResultsByDay>
   <MeetingDurationInMinutes>...</MeetingDurationInMinutes>
   <MinimumSuggestionQuality>...</MinimumSuggestionQuality>
   <SuggestionIntervalInMinutes>...</SuggestionIntervalInMinutes>
   <DetailedSuggestionsWindow>...</DetailedSuggestionsWindow>
   <CurrentMeetingTime>...</CurrentMeetingTime>
   <GlobalObjectId>...</GlobalObjectId>
</SuggestionsViewOptions>
```

 **SuggestionsViewOptionsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GoodThreshold](goodthreshold.md) <br/> |Gibt den Prozentsatz der Teilnehmer, die den Zeitraum an, für den Zeitraum als eine gute Vorgeschlagene Besprechungszeit qualifizieren öffnen benötigen.  <br/> |
|[' MaximumResultsByDay '](maximumresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Besprechung pro Tag in der Antwort zurückgegeben.  <br/> |
|[' MaximumNonWorkHourResultsByDay '](maximumnonworkhourresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb der regulären Arbeitszeit pro Tag.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Gibt die Länge der Besprechung, die vorgeschlagen werden.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Gibt die Qualität der Besprechungsvorschläge in der Antwort zurückgegeben werden soll.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Stellt die Anfangszeit der eine Besprechung, die Sie mit der vorgeschlagenen Besprechung aktualisieren möchten Zeit Ergebnisse.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |Dieses Element wird nicht verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet. Dies ist eine Stammelements.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist nicht erforderlich, und kann nur einmal auftreten, wenn verwendet. Dieser Wert kann null sein, wenn der Wert des Elements [FreeBusyViewOptions](freebusyviewoptions.md) nicht null ist. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

