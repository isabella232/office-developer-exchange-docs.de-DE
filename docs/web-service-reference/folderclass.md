---
title: FolderClass
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderClass
api_type:
- schema
ms.assetid: 0041d135-2869-4612-89a5-d1aa86aa1093
description: Das FolderClass-Element darstellt, die Ordner-Klasse für einen Ordner.
ms.openlocfilehash: 87be00563d0375abebf32159ff38d62d03112b95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758500"
---
# <a name="folderclass"></a>FolderClass

Das **FolderClass** -Element darstellt, die Ordner-Klasse für einen Ordner. 
  
```xml
<FolderClass/>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach an.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Ordner Klassen beginnen normalerweise mit "IPF."
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

