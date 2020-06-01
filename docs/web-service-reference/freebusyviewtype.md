---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: Das FreeBusyViewType-Element stellt den Typ der Frei/Gebucht-Informationen dar, die in der Antwort zurückgegeben werden.
ms.openlocfilehash: 3556ad236693ac9aa018b8aa3af7843765da6aa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459567"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

Das **FreeBusyViewType** -Element stellt den Typ der Frei/Gebucht-Informationen dar, die in der Antwort zurückgegeben werden. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[FreeBusyViewType](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
```

 **FreeBusyViewType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FreeBusyView](freebusyview.md) <br/> |Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Dieser Wert ist für Anforderungen ungültig. Dieser Wert ist für Antworten gültig.  <br/> |
|MergedOnly  <br/> |Stellt einen aggregierten frei/gebucht-Datenstrom dar. Bei gesamtstrukturübergreifenden Szenarien, in denen für den Zielbenutzer in einer Gesamtstruktur kein Verfügbarkeitsdienst konfiguriert ist, ruft der Verfügbarkeitsdienst des Anforderers die Frei/Gebucht-Informationen des Zielbenutzers aus dem öffentlichen Frei/Gebucht-Ordner ab. Da öffentliche Ordner nur Frei/Gebucht-Informationen im zusammengeführten Formular speichern, ist **MergedOnly** die einzigen verfügbaren Informationen.  <br/> |
|FreeBusy  <br/> |Stellt die Legacy Statusinformationen dar: frei, beschäftigt, vorläufig und OOF. Dies umfasst auch die Anfangs-und Endzeiten der Termine. Diese Ansicht ist reicher als die Legacy-Frei/Gebucht-Ansicht, da anstelle eines aggregierten frei/gebucht-Streams einzelne Start-und Endzeiten für Besprechungen bereitgestellt werden.  <br/> |
|FreeBusyMerged  <br/> |Stellt alle Eigenschaften in **freebusy** mit einem Datenstrom von zusammengeführten Informationen zur Verfügbarkeit von Frei/Gebucht-Informationen dar.  <br/> |
|Detaillierte  <br/> |Stellt die Legacy Statusinformationen dar: frei, beschäftigt, vorläufig und OOF; die Start-und Endzeit Zeiten der Termine; und verschiedene Eigenschaften des Termins wie Betreff, Ort und Wichtigkeit. In dieser angeforderten Ansicht wird die maximale Menge an Informationen zurückgegeben, für die der anfordernde Benutzer privilegiert ist. Wenn zusammengeführte Frei/Gebucht-Informationen nur verfügbar sind, wie beim Anfordern von Informationen für Benutzer in einer Microsoft Exchange Server 2003 Gesamtstruktur, wird **MergedOnly** zurückgegeben. Andernfalls wird **freebusy** oder **detailed** zurückgegeben.  <br/> Wenn **detaillierte** für eine Verteilerliste angegeben ist, werden die Frei/Gebucht-Informationen für die Mitglieder der Liste zusammengeführt, und **MergedOnly** wird zurückgegeben.  <br/> |
|DetailedMerged  <br/> |Stellt alle Eigenschaften im **Detail** mit einem Stream von zusammengeführten Informationen zur Frei/Gebucht-Verfügbarkeit dar. Wenn nur zusammengeführte Frei/Gebucht-Informationen verfügbar sind, beispielsweise wenn das Postfach auf einem Computer mit Exchange 2003 vorhanden ist, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusyMerged** oder **DetailedMerged** zurückgegeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist erforderlich, wenn das [FreeBusyView](freebusyview.md) -Element verwendet wird. Der Typ der zurückgegebenen Frei/Gebucht-Informationen wird im [RequestedView](requestedview.md) -Element festgelegt. Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
In der folgenden Tabelle wird gezeigt, was für die verschiedenen Ansichtstypen und die entsprechende MAPI-Eigenschaft zurückgegeben wird. Jeder Ansichtstyp basiert auf dem vorherigen Ansichtstyp.
  
|**FreeBusyViewType**|**Eigenschaften**|**MAPI Calendar-Eigenschaft**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Klassischer Status  <br/> |Eigenschaftstag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Arbeitsstunden  <br/> ||
|**FreeBusy** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Klassischer Status  <br/> |Eigenschaftstag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Arbeitsstunden  <br/> ||
|**FreeBusyMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detaillierte** <br/> |Klassischer Status  <br/> |Eigenschaftstag (0x80860003)  <br/> |
|**Detaillierte** <br/> |Arbeitsstunden  <br/> ||
|**Detaillierte** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**Detaillierte** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**Detaillierte** <br/> |Betreff  <br/> |PR_SUBJECT  <br/> |
|**Detaillierte** <br/> |Standort  <br/> |PR_LOCATION  <br/> |
|**Detaillierte** <br/> |Entry-ID (sofern nicht privat)  <br/> ||
|**Detaillierte** <br/> |Private Kennzeichnung  <br/> ||
|**Detaillierte** <br/> |Ismeeting  <br/> ||
|**Detaillierte** <br/> |IsRecurring  <br/> ||
|**Detaillierte** <br/> |Isexception  <br/> ||
|**Detaillierte** <br/> |Reminder  <br/> ||
|**Detaillierte** <br/> |Abwesenheitsnachricht (falls erforderlich)  <br/> ||
|**DetailedMerged** <br/> |Klassischer Status  <br/> |Eigenschaftstag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Arbeitsstunden  <br/> ||
|**DetailedMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Betreff  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Standort  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entry-ID (sofern nicht privat)  <br/> ||
|**DetailedMerged** <br/> |Private Kennzeichnung  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |Ismeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |Isexception  <br/> ||
|**DetailedMerged** <br/> |Reminder  <br/> ||
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

