---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: Das ArchiveTag-Element gibt die Aufbewahrungs-ID des Archiv-Tags an, das für ein Element oder einen Ordner festgelegt wurde.
ms.openlocfilehash: 23167f3c96a6756fe4c6d915a4de91e815e620d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464763"
---
# <a name="archivetag"></a>ArchiveTag

Das **ArchiveTag** -Element gibt die Aufbewahrungs-ID des Archiv-Tags an, das für ein Element oder einen Ordner festgelegt wurde. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Isexplicit** <br/> |Gibt an, ob die Aufbewahrungsrichtlinie explizit für ein Element oder einen Ordner festgelegt wird oder ob Sie von einem übergeordneten Ordner geerbt wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Kontaktelement im Exchange-Speicher.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner dar, der in einem Postfach enthalten ist.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Folder](folder.md) <br/> |Definiert einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Element in der Exchange-Informationsspeicher dar.  <br/> |
|[Nachricht](message-ex15websvcsotherref.md) <br/> |Stellt eine Microsoft Exchange e-Mail-Nachricht dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Informationsspeicher dar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner dar, der in einem Postfach enthalten ist.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner dar, der in einem Postfach enthalten ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **ArchiveTag** -Elements ist eine GUID, die die Aufbewahrungsrichtlinie identifiziert. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

