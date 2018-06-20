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
description: Das Element FreeBusyViewType stellt den Typ der Frei/Gebucht-Informationen in der Antwort zurückgegeben.
ms.openlocfilehash: fe965d062f72d99dff7148f4d00b12fd8c4e1366
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758559"
---
# <a name="freebusyviewtype"></a>FreeBusyViewType

Das Element **FreeBusyViewType** stellt den Typ der Frei/Gebucht-Informationen in der Antwort zurückgegeben. 
  
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
|[FreeBusyView](freebusyview.md) <br/> |Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Die folgende Tabelle enthält die möglichen Werte für dieses Element.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Dieser Wert ist nicht gültig für Anfragen. Dieser Wert gilt für Antworten.  <br/> |
|MergedOnly  <br/> |Stellt einen aggregierten Frei/Gebucht-Stream. In gesamtstrukturübergreifenden-Szenarien, in denen die Zielbenutzer in einer Gesamtstruktur keine Verfügbarkeitsdienst konfiguriert haben, ruft der Verfügbarkeitsdienst des Antragstellers des Zielbenutzers Frei/Gebucht-Informationen aus dem öffentlichen Ordner mit Frei/Gebucht-Informationen. Da Öffentliche Ordner nur Frei/Gebucht-Informationen in zusammengeführte Formular gespeichert werden sollen, ist **MergedOnly** die einzige verfügbare Informationen.  <br/> |
|FreeBusy  <br/> |Stellt die Vorversion Statusinformationen: frei, gebucht, mit Vorbehalt und OOF. Dazu gehören auch die Start-/Endzeiten der Termine. Diese Ansicht ist umfangreicher als die Vorversion Frei/Gebucht-Informationen anzeigen, da einzelne Besprechung starten und beenden Sie Zeiten anstelle einer aggregierten Frei/Gebucht-Stream bereitgestellt.  <br/> |
|FreeBusyMerged  <br/> |Stellt alle Eigenschaften in **FreeBusy** mit einen Datenstrom zusammengeführten Frei/Gebucht-Informationen zu Ihrer Verfügbarkeit einsehen.  <br/> |
|Detailliert  <br/> |Stellt die Vorversion Statusinformationen: frei, gebucht, mit Vorbehalt und OOF; die Start-/Endzeiten der Termine; und verschiedene Eigenschaften des Termins wie Betreff, Ort und Bedeutung. Diese angeforderten Ansicht zurück die maximale Datenmenge, der anfordernde Benutzer Berechtigungen aufweist. Wenn zusammengeführten Frei/Gebucht-Informationen nur verfügbar ist, werden als mit anfordernde Informationen für Benutzer in einer Microsoft Exchange Server 2003-Gesamtstruktur **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusy** oder **Detailed** zurückgegeben werden soll.  <br/> Wenn für eine Verteilerliste **Detailed** angegeben ist, wird die Frei/Gebucht-Informationen für die Mitglieder der Liste zusammengeführt, und **MergedOnly** wird zurückgegeben.  <br/> |
|DetailedMerged  <br/> |Stellt alle Eigenschaften in **Detailed** mit einen Datenstrom zusammengeführten Frei/Gebucht-Informationen zu Ihrer Verfügbarkeit einsehen. Wenn nur zusammengeführten Frei/Gebucht-Informationen verfügbar, z. B. sind, wenn das Postfach auf einem Computer mit Exchange 2003 vorhanden ist, wird **MergedOnly** zurückgegeben. Andernfalls wird **FreeBusyMerged** oder **DetailedMerged** zurückgegeben werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist erforderlich, wenn das [FreeBusyView](freebusyview.md) -Element verwendet wird. Der Typ der zurückgegebenen Frei/Gebucht-Informationen wird im [RequestedView](requestedview.md) -Element festgelegt. Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
Die folgende Tabelle zeigt, was für die anderen Ansichtstypen und der entsprechenden MAPI-Eigenschaft zurückgegeben wird. Jede Ansichtstyp baut auf der vorhergehenden Ansichtstyp.
  
|**FreeBusyViewType**|**Eigenschaften**|**MAPI-Calendar-Eigenschaft**|
|:-----|:-----|:-----|
|**MergedOnly** <br/> |MergedFreeBusyStream  <br/> ||
|**FreeBusy** <br/> |Klassische status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusy** <br/> |Arbeitszeiten  <br/> ||
|**FreeBusy** <br/> |Startzeit  <br/> |PR_START_DATE  <br/> |
|**FreeBusy** <br/> |Endzeit  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |Klassische status  <br/> |PropTag (0x80860003)  <br/> |
|**FreeBusyMerged** <br/> |Arbeitszeiten  <br/> ||
|**FreeBusyMerged** <br/> |Startzeit  <br/> |PR_START_DATE  <br/> |
|**FreeBusyMerged** <br/> |Endzeit  <br/> |PR_END_DATE  <br/> |
|**FreeBusyMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**Detaillierte** <br/> |Klassische status  <br/> |PropTag (0x80860003)  <br/> |
|**Detaillierte** <br/> |Arbeitszeiten  <br/> ||
|**Detaillierte** <br/> |Startzeit  <br/> |PR_START_DATE  <br/> |
|**Detaillierte** <br/> |Endzeit  <br/> |PR_END_DATE  <br/> |
|**Detaillierte** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**Detaillierte** <br/> |Speicherort  <br/> |PR_LOCATION  <br/> |
|**Detaillierte** <br/> |Eintrag Id(unless private)  <br/> ||
|**Detaillierte** <br/> |Private Kennzeichnung  <br/> ||
|**Detaillierte** <br/> |IsMeeting  <br/> ||
|**Detaillierte** <br/> |IsRecurring  <br/> ||
|**Detaillierte** <br/> |IsException  <br/> ||
|**Detaillierte** <br/> |IsReminderSet  <br/> ||
|**Detaillierte** <br/> |Abwesenheitsnotiz (falls erforderlich)  <br/> ||
|**DetailedMerged** <br/> |Klassische status  <br/> |PropTag (0x80860003)  <br/> |
|**DetailedMerged** <br/> |Arbeitszeiten  <br/> ||
|**DetailedMerged** <br/> |Startzeit  <br/> |PR_START_DATE  <br/> |
|**DetailedMerged** <br/> |Endzeit  <br/> |PR_END_DATE  <br/> |
|**DetailedMerged** <br/> |Subject  <br/> |PR_SUBJECT  <br/> |
|**DetailedMerged** <br/> |Speicherort  <br/> |PR_LOCATION  <br/> |
|**DetailedMerged** <br/> |Eintrag Id(unless private)  <br/> ||
|**DetailedMerged** <br/> |Private Kennzeichnung  <br/> ||
|**DetailedMerged** <br/> |MergedFreeBusyStream  <br/> ||
|**DetailedMerged** <br/> |IsMeeting  <br/> ||
|**DetailedMerged** <br/> |IsRecurring  <br/> ||
|**DetailedMerged** <br/> |IsException  <br/> ||
|**DetailedMerged** <br/> |IsReminderSet  <br/> ||
   
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

