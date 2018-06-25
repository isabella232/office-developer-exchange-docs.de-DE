---
title: MeetingSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6012063-eb67-4e83-a4a6-33482685083f
description: Das MeetingSuggestion-Element gibt eine vorgeschlagene Besprechung.
ms.openlocfilehash: 35b618b32101ea36c35d87ca0737e4a7e04eb3a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830444"
---
# <a name="meetingsuggestion"></a>MeetingSuggestion

Das **MeetingSuggestion** -Element gibt eine vorgeschlagene Besprechung. 
  
```XML
<MeetingSuggestion>
   <Attendees/>
   <Location/>
   <Subject/>
   <MeetingString/>
   <StartTime/>
   <EndTime/>
</MeetingSuggestion>
```

 **MeetingSuggestionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Teilnehmer](attendees.md) | [Speicherort](location.md) | [Betreff](subject.md) | ["meetingstring"](meetingstring.md) | [StartTime](starttime.md) | [EndTime](endtime.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

["Meetingsuggestions"](meetingsuggestions.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

