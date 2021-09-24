---
title: RequestedView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RequestedView
api_type:
- schema
ms.assetid: e2b4cf8c-5d43-4cd8-b86d-cc27a5d2f095
description: Das RequestedView-Element definiert den Typ der Kalenderinformationen, die ein Client anfordert.
ms.openlocfilehash: 350922a7fef90c26ace0ef8be07ebb866d304eb3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509476"
---
# <a name="requestedview"></a>RequestedView

Das **RequestedView-Element** definiert den Typ der Kalenderinformationen, die ein Client anfordert. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[FreeBusyViewOptions](freebusyviewoptions.md)
  
[RequestedView](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
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
|[FreeBusyViewOptions](freebusyviewoptions.md) <br/> |Gibt den Typ der Frei/Gebucht-Informationen an, die in der Antwort zurückgegeben werden.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Dieser Wert ist für Anforderungen ungültig. Dieser Wert gilt für Antworten.  <br/> |
|MergedOnly  <br/> |Stellt einen aggregierten Frei/Gebucht-Datenstrom dar. In gesamtstrukturübergreifenden Szenarien, in denen der Zielbenutzer in einer Gesamtstruktur keinen Verfügbarkeitsdienst konfiguriert hat, ruft der Verfügbarkeitsdienst des Anforderers die Frei/Gebucht-Informationen des Zielbenutzers aus dem öffentlichen Frei/Gebucht-Ordner ab. Da öffentliche Ordner nur Frei/Gebucht-Informationen in zusammengeführter Form speichern, sind **MergedOnly** die einzigen verfügbaren Informationen.  <br/> |
|FreeBusy  <br/> |Stellt die Statusinformationen der Vorversion dar: frei, beschäftigt, mit Vorbehalt und OOF. Dies umfasst auch die Anfangs-/Endzeiten der Termine. Diese Ansicht ist umfangreicher als die ältere Frei/Gebucht-Ansicht, da einzelne Besprechungsanfangs- und -endzeiten anstelle eines aggregierten Frei/Gebucht-Datenstroms bereitgestellt werden.  <br/> |
|FreeBusyMerged  <br/> |Stellt alle Eigenschaften in **FreeBusy** mit einem Datenstrom zusammengeführter Frei/Gebucht-Informationen dar.  <br/> |
|Detaillierte  <br/> |Stellt die Statusinformationen der Vorversion dar: frei, beschäftigt, mit Vorbehalt und OOF; die Start-/Endzeiten der Termine; und verschiedene Eigenschaften des Termins, z. B. Betreff, Ort und Wichtigkeit. Diese angeforderte Ansicht gibt die maximale Anzahl von Informationen zurück, für die der anfordernde Benutzer berechtigt ist. Wenn zusammengeführte Frei/Gebucht-Informationen nur verfügbar sind, wie beim Anfordern von Informationen für Benutzer in einer Microsoft Exchange Server 2003-Gesamtstruktur, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusy** oder **Detailed** zurückgegeben.  <br/> |
|DetailedMerged  <br/> |Stellt alle Eigenschaften in **Detail** mit einem Datenstrom zusammengeführter Frei/Gebucht-Informationen dar. Wenn zusammengeführte Frei/Gebucht-Informationen nur verfügbar sind, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusyMerged** oder **DetailedMerged** zurückgegeben.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der von diesem Element festgelegte Wert wird mit dem [FreeBusyViewType-Element](freebusyviewtype.md) in der Antwort zurückgegeben. 
  
Die folgende Tabelle zeigt, was für die verschiedenen Ansichtstypen und die entsprechende MAPI-Eigenschaft zurückgegeben wird. Jeder Ansichtstyp baut auf dem früheren Ansichtstyp auf.
  
|**Frei/Gebucht-Ansichtstyp**|**Eigenschaften**|**MAPI Calendar-Eigenschaft**|
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


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

