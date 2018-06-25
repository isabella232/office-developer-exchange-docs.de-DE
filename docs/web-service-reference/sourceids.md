---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: Das SourceIds-Element enthält die Source-Bezeichner konvertiert.
ms.openlocfilehash: c9ee9fd01367f714e1cb3770e2be5161cb45d98f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831522"
---
# <a name="sourceids"></a>SourceIds

Das **SourceIds** -Element enthält die Source-Bezeichner konvertiert. 
  
[ConvertId](convertid.md)
  
[SourceIds](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 **NonEmptyArrayOfAlternateIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AlternateId](alternateid.md) <br/> |Beschreibt einen Bezeichner Elements oder Ordners zu konvertieren.  <br/> |
|[AlternatePublicFolderId](alternatepublicfolderid.md) <br/> |Beschreibt einen Bezeichner für Öffentliche Ordner zu konvertieren.  <br/> |
|[AlternatePublicFolderItemId](alternatepublicfolderitemid.md) <br/> |Beschreibt einen Bezeichner für Öffentliche Ordner zu konvertieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConvertId](convertid.md) <br/> |Definiert eine Anforderung zum Element und Ordner Bezeichner zwischen Exchange unterstützt Formate konvertieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ConvertId-Vorgang](convertid-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Konvertieren von Bezeichnern](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

