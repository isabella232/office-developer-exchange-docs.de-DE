---
title: MeetingSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d6012063-eb67-4e83-a4a6-33482685083f
description: Das MeetingSuggestion-Element gibt eine vorgeschlagene Besprechung an.
ms.openlocfilehash: 20523a77fc9fcdf22c837f2e4101ed699e1d4a7b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532489"
---
# <a name="meetingsuggestion"></a>MeetingSuggestion

Das **MeetingSuggestion-Element** gibt eine vorgeschlagene Besprechung an. 
  
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

[Teilnehmer](attendees.md)  |  [Speicherort](location.md)  |  [Betreff](subject.md)  |  [MeetingString](meetingstring.md)  |  [StartTime](starttime.md)  |  [EndTime](endtime.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MeetingSuggestions](meetingsuggestions.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

