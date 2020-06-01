---
title: FolderSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderSize
api_type:
- schema
ms.assetid: 27e5f0cd-e23a-4ddd-943a-9f17bf0fd87b
description: Das Folders-Element beschreibt die Gesamtgröße aller Inhalte eines verwalteten Ordners.
ms.openlocfilehash: 8ed493cfb0c2cabd02d28354c115a73662992473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461338"
---
# <a name="foldersize"></a>FolderSize

Das **Folders** -Element beschreibt die Gesamtgröße aller Inhalte eines verwalteten Ordners. 
  
```xml
<FolderSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die Gesamtgröße des Ordners in Megabytes dar.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

