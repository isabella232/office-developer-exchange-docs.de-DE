---
title: SetFolderField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetFolderField
api_type:
- schema
ms.assetid: 8c69db7b-54b5-4ae2-abca-4d6e0937a790
description: Das SetFolderField-Element stellt ein Update, das den Wert für eine einzelne Eigenschaft für einen Ordner in einem Vorgang UpdateFolder fest.
ms.openlocfilehash: 1919c335197c83999875a17397e9c9d4405d1e3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831407"
---
# <a name="setfolderfield"></a>SetFolderField

Das **SetFolderField** -Element stellt ein Update, das den Wert für eine einzelne Eigenschaft für einen Ordner in einem Vorgang UpdateFolder fest. 
  
```xml
<SetFolderField>
   <FieldURI/>
   <Folder/>
</SetFolderField>
```

 **SetFolderFieldType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert extended MAPI-Eigenschaften.  <br/> |
|[Folder](folder.md) <br/> |Gibt einen Ordner aktualisieren.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner, der in einem Postfach enthalten ist.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner, der in einem Postfach enthalten ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Updates (Ordner)](updates-folder.md) <br/> |Enthält eine Reihe von Elementen, die definiert, anfügen, festlegen und Löschen von Änderungen an den Eigenschaften des Ordners.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die Eigenschaft vorhanden ist, wird der Wert der Eigenschaft auf den angegebenen Wert festgelegt. Wenn die Eigenschaft nicht vorhanden ist, wird die Eigenschaft mit dem angegebenen Wert erstellt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateFolder-Vorgang](updatefolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

