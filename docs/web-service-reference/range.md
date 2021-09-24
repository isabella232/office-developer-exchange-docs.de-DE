---
title: Bereich
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Das Range-Element gibt einen Bereich von Kalenderelementvorkommen für ein wiederholtes Kalenderelement an.
ms.openlocfilehash: 0d16dad24dda48f084b3011d7b96eb719431d9da
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519100"
---
# <a name="range"></a>Bereich

Das **Range-Element** gibt einen Bereich von Kalenderelementvorkommen für ein wiederholtes Kalenderelement an. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Start** <br/> |Der Textwert  des Start-Attributs ist das Startdatum des Wiederkehrenden Elementbereichs. Dies ist ein **dateTime-Wert.**  <br/> |
|**End** <br/> |Der Textwert  des End-Attributs ist das Enddatum des Wiederkehrenden Elementbereichs. Dies ist ein **dateTime-Wert.**  <br/> |
|**Count** <br/> |Der Textwert  des Count-Attributs ist die Anzahl der Vorkommen des Wiederkehrenden Elements. Dies ist ein **ganzzahliger** Wert.  <br/> |
|**CompareOriginalStartTime** <br/> |Der Textwert **"true"** für das **CompareOriginalStartTime-Attribut** gibt an, dass der Client die ursprüngliche Startzeit mit der neuen Startzeit vergleichen sollte. Der Wert **"false"** gibt an, dass der Client die ursprüngliche Startzeit nicht mit der neuen Startzeit vergleichen muss.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Ranges](ranges.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

