---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: Das FreeBusyViewType-Element stellt den Typ der Frei/Gebucht-Informationen dar, die in der Antwort zurückgegeben werden.
ms.openlocfilehash: 6eec490b39ccb9c02e7a16c8da7cfdd57f9b92c5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509924"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

Das **FreeBusyViewType-Element** stellt den Typ der Frei/Gebucht-Informationen dar, die in der Antwort zurückgegeben werden. 
  
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
|Keine  <br/> |Dieser Wert ist für Anforderungen ungültig. Dieser Wert gilt für Antworten.  <br/> |
|MergedOnly  <br/> |Stellt einen aggregierten Frei/Gebucht-Datenstrom dar. In gesamtstrukturübergreifenden Szenarien, in denen der Zielbenutzer in einer Gesamtstruktur keinen Verfügbarkeitsdienst konfiguriert hat, ruft der Verfügbarkeitsdienst des Anforderers die Frei/Gebucht-Informationen des Zielbenutzers aus dem öffentlichen Frei/Gebucht-Ordner ab. Da öffentliche Ordner nur Frei/Gebucht-Informationen in zusammengeführter Form speichern, sind **MergedOnly** die einzigen verfügbaren Informationen.  <br/> |
|FreeBusy  <br/> |Stellt die Statusinformationen der Vorversion dar: frei, beschäftigt, mit Vorbehalt und OOF. Dies umfasst auch die Anfangs-/Endzeiten der Termine. Diese Ansicht ist umfangreicher als die ältere Frei/Gebucht-Ansicht, da einzelne Besprechungsanfangs- und -endzeiten anstelle eines aggregierten Frei/Gebucht-Datenstroms bereitgestellt werden.  <br/> |
|FreeBusyMerged  <br/> |Stellt alle Eigenschaften in **FreeBusy** mit einem Datenstrom zusammengeführter Frei/Gebucht-Verfügbarkeitsinformationen dar.  <br/> |
|Detaillierte  <br/> |Stellt die Statusinformationen der Vorversion dar: frei, beschäftigt, mit Vorbehalt und OOF; die Start-/Endzeiten der Termine; und verschiedene Eigenschaften des Termins, z. B. Betreff, Ort und Wichtigkeit. Diese angeforderte Ansicht gibt die maximale Anzahl von Informationen zurück, für die der anfordernde Benutzer berechtigt ist. Wenn zusammengeführte Frei/Gebucht-Informationen nur verfügbar sind, wie beim Anfordern von Informationen für Benutzer in einer Microsoft Exchange Server 2003-Gesamtstruktur, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusy** oder **Detailed** zurückgegeben.  <br/> Wenn  Detail für eine Verteilerliste angegeben ist, werden die Frei/Gebucht-Informationen für die Mitglieder der Liste zusammengeführt, und **MergedOnly** wird zurückgegeben.  <br/> |
|DetailedMerged  <br/> |Stellt alle Eigenschaften in **Detail** mit einem Datenstrom zusammengeführter Frei/Gebucht-Verfügbarkeitsinformationen dar. Wenn nur zusammengeführte Frei/Gebucht-Informationen verfügbar sind, z. B. wenn das Postfach auf einem Computer mit Exchange 2003 vorhanden ist, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusyMerged** oder **DetailedMerged** zurückgegeben.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist erforderlich, wenn das [FreeBusyView-Element](freebusyview.md) verwendet wird. Der Typ der zurückgegebenen Frei/Gebucht-Informationen wird im [RequestedView-Element](requestedview.md) festgelegt. Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Die folgende Tabelle zeigt, was für die verschiedenen Ansichtstypen und die entsprechende MAPI-Eigenschaft zurückgegeben wird. Jeder Ansichtstyp baut auf dem früheren Ansichtstyp auf.
  
|**FreeBusyViewType**|**Eigenschaften**|**MAPI Calendar-Eigenschaft**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Klassischer Status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Arbeitszeit  <br/> ||
|**FreeBusy** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Klassischer Status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Arbeitszeit  <br/> ||
|**FreeBusyMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detaillierte** <br/> |Klassischer Status  <br/> |PropTag (0x80860003)  <br/> |
|**Detaillierte** <br/> |Arbeitszeit  <br/> ||
|**Detaillierte** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**Detaillierte** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**Detaillierte** <br/> |Betreff  <br/> |PR_SUBJECT  <br/> |
|**Detaillierte** <br/> |Ort  <br/> |PR_LOCATION  <br/> |
|**Detaillierte** <br/> |Entry-Id(außer privat)  <br/> ||
|**Detaillierte** <br/> |Private Flag  <br/> ||
|**Detaillierte** <br/> |IsMeeting  <br/> ||
|**Detaillierte** <br/> |IsRecurring  <br/> ||
|**Detaillierte** <br/> |IsException  <br/> ||
|**Detaillierte** <br/> |IsReminderSet  <br/> ||
|**Detaillierte** <br/> |Out of Office Message (if requested)  <br/> ||
|**DetailedMerged** <br/> |Klassischer Status  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Arbeitszeit  <br/> ||
|**DetailedMerged** <br/> |Start time  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |End time  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Betreff  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Ort  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Entry-Id(außer privat)  <br/> ||
|**DetailedMerged** <br/> |Private Flag  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
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


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

