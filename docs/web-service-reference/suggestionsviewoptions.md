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
description: Das SuggestionsViewOptions-Element enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.
ms.openlocfilehash: f584b19997f98760bd4e438dcd48a5c18cc63e4b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44433994"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

Das **SuggestionsViewOptions** -Element enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen. 
  
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
|[GoodThreshold](goodthreshold.md) <br/> |Gibt den Prozentsatz der Teilnehmer an, für den der Zeitraum, der für den Zeitraum geöffnet sein muss, als eine gute vorgeschlagene Besprechungszeit qualifiziert werden muss.  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden.  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb regulärer Arbeitsstunden pro Tag an.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Gibt die Länge der Besprechung an, die vorgeschlagen werden soll.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Gibt die Qualität der Besprechungsvorschläge an, die in der Antwort zurückgegeben werden sollen.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt den Zeitraum an, der nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Stellt die Startzeit einer Besprechung dar, die mit den Ergebnissen der vorgeschlagenen Besprechungszeit aktualisiert werden soll.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |Dieses Element wird nicht verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Informationen zur Benutzerverfügbarkeit verwendet werden. Dies ist ein Stammelement.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist nicht erforderlich und kann nur einmal auftreten, wenn es verwendet wird. Dieser Wert kann NULL sein, wenn der Wert des [FreeBusyViewOptions](freebusyviewoptions.md) -Elements nicht NULL ist. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

