---
title: DetailedSuggestionsWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: Das DetailedSuggestionsWindow-Element gibt die Zeitspanne an, die nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.
ms.openlocfilehash: 45d582f2642c0e3d8f6330b09946230c8842618d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467844"
---
# <a name="detailedsuggestionswindow"></a>DetailedSuggestionsWindow

Das **DetailedSuggestionsWindow** -Element gibt die Zeitspanne an, die nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md) 
- [SuggestionsViewOptions](suggestionsviewoptions.md) 
- [DetailedSuggestionsWindow](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 **Duration**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Stellt den Anfang der abgefragten Zeitspanne dar, um detaillierte Informationen zu vorgeschlagenen Besprechungszeiten zu erhalten.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende der abgefragten Zeitspanne dar, um detaillierte Informationen zu vorgeschlagenen Besprechungszeiten zu erhalten.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist nicht erforderlich.
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

