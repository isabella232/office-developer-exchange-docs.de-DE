---
title: SuggestionsViewOptions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionsViewOptions
api_type:
- schema
ms.assetid: bb04ae38-e62d-4a69-a479-8ff326ca726e
description: Das SuggestionsViewOptions-Element enthält die Optionen zum Abrufen von Besprechungsvorschlagsinformationen.
ms.openlocfilehash: ba3591b88e581d45c811100a53b0a74e4bb8e010
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522614"
---
# <a name="suggestionsviewoptions"></a>SuggestionsViewOptions

Das **SuggestionsViewOptions-Element** enthält die Optionen zum Abrufen von Besprechungsvorschlagsinformationen. 
  
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
|[GoodThreshold](goodthreshold.md) <br/> |Gibt den Prozentsatz der Teilnehmer an, für die der Zeitraum für den Zeitraum geöffnet sein muss, um sich als gute vorgeschlagene Besprechungszeit zu qualifizieren.  <br/> |
|[MaximumResultsByDay](maximumresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden.  <br/> |
|[MaximumNonWorkHourResultsByDay](maximumnonworkhourresultsbyday.md) <br/> |Gibt die Anzahl der vorgeschlagenen Ergebnisse für Besprechungszeiten außerhalb der regulären Arbeitszeiten pro Tag an.  <br/> |
|[MeetingDurationInMinutes](meetingdurationinminutes.md) <br/> |Gibt die Länge der Besprechung an, die vorgeschlagen werden soll.  <br/> |
|[MinimumSuggestionQuality](minimumsuggestionquality.md) <br/> |Gibt die Qualität von Besprechungsvorschlägen an, die in der Antwort zurückgegeben werden sollen.  <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt die Zeitspanne an, für die detaillierte Informationen zu vorgeschlagenen Besprechungszeiten abgefragt werden.  <br/> |
|[CurrentMeetingTime](currentmeetingtime.md) <br/> |Stellt die Startzeit einer Besprechung dar, die Sie mit den vorgeschlagenen Besprechungszeitergebnissen aktualisieren möchten.  <br/> |
|[GlobalObjectId](globalobjectid.md) <br/> |Dieses Element wird nicht verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Benutzerverfügbarkeitsinformationen verwendet werden. Dies ist ein Stammelement.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist nicht erforderlich und kann nur einmal auftreten, wenn es verwendet wird. Dieser Wert kann NULL sein, wenn der Wert des [FreeBusyViewOptions-Elements](freebusyviewoptions.md) nicht NULL ist. 
  
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


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

