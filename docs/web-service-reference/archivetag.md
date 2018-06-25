---
title: ArchiveTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c4cb0718-37cd-41aa-86e7-b492c4bb86aa
description: Das ArchiveTag-Element gibt den Aufbewahrung Bezeichner des Archivs Tags auf eines Elements oder Ordners festlegen.
ms.openlocfilehash: ae9c7d512981af3bf564bcb73a9a27c5c78217fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757377"
---
# <a name="archivetag"></a>ArchiveTag

Das **ArchiveTag** -Element gibt den Aufbewahrung Bezeichner des Archivs Tags auf eines Elements oder Ordners festlegen. 
  
```XML
<ArchiveTag IsExplicit=""></ArchiveTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**IsExplicit** <br/> |Gibt an, ob die Aufbewahrungsrichtlinie auf eines Elements oder Ordners explizit festgelegt ist oder ob es von einem übergeordneten Ordner geerbt wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Kontaktelement im Exchange-Speicher.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner, der in einem Postfach enthalten ist.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Folder](folder.md) <br/> |Definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Element im Exchange-Speicher.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Microsoft Exchange-e-Mail-Nachricht dar.  <br/> |
|[PostItem-Objekt](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Speicher.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner, der in einem Postfach enthalten ist.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **ArchiveTag** -Elements ist eine GUID, die Aufbewahrungsrichtlinie identifiziert. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

