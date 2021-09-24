---
title: DisplayName (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DisplayName
api_type:
- schema
ms.assetid: e7efbbe1-6629-4d11-bed1-ed899e3f9d77
description: Das DisplayName-Element definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreterbenutzers, eines Speicherorts oder einer Regel.
ms.openlocfilehash: 3fc0faca0425bc6de3f71c154926991d922c8a79
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520863"
---
# <a name="displayname-string"></a>DisplayName (Zeichenfolge)

Das **DisplayName-Element** definiert den Anzeigenamen eines Ordners, Kontakts, einer Verteilerliste, eines Stellvertreterbenutzers, eines Speicherorts oder einer Regel. 
  
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
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontaktordner in einem Postfach dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Ordner](folder.md) <br/> |Stellt einen Ordner in einem Postfach dar.  <br/> |
|[Regel (RuleType)](rule-ruletype.md) <br/> |Stellt eine Regel im Postfach eines Benutzers dar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach dar.  <br/> |
|[UserId](userid.md) <br/> |Identifiziert einen Stellvertreterbenutzer oder einen Benutzer, der über Ordnerzugriffsberechtigungen verfügt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der den Anzeigenamen darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Dieses folgende Beispiel zeigt, wie Sie einen neuen Ordner erstellen und den DisplayName des Ordners auf "TestFolder" festlegen.
  
```cs
FolderType folder = new FolderType();
folder.DisplayName = "TestFolder";
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

