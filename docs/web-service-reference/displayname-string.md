---
title: DisplayName (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DisplayName
api_type:
- schema
ms.assetid: e7efbbe1-6629-4d11-bed1-ed899e3f9d77
description: Das DisplayName-Element definiert den Anzeigenamen eines Ordners, Kontakt, Verteilerliste, Stellvertretungsbenutzers, Standort oder Regel.
ms.openlocfilehash: 53f4e083d9e6617206e383d4408e08ed7ea0fe08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758048"
---
# <a name="displayname-string"></a>DisplayName (Zeichenfolge)

Das **DisplayName** -Element definiert den Anzeigenamen eines Ordners, Kontakt, Verteilerliste, Stellvertretungsbenutzers, Standort oder Regel. 
  
```XML
<DisplayName/>
```

 **String**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach an.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einem Kontaktordner in einem Postfach an.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[Regel (RuleType)](rule-ruletype.md) <br/> |Stellt eine Regel in dem Postfach eines Benutzers.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[Benutzer-ID](userid.md) <br/> |Identifiziert ein Stellvertreter oder ein Benutzer mit Zugriffsberechtigungen für Ordner.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der den Anzeigenamen darstellt ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird gezeigt, wie auf einen neuen Ordner erstellen und die DisplayName des Ordners "TestFolder" festgelegt.
  
```cs
FolderType folder = new FolderType();
folder.DisplayName = "TestFolder";
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

