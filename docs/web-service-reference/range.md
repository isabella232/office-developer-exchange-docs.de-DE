---
title: Bereich
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Das Range-Element gibt einen Bereich von Kalenderelement Vorkommen für ein wiederholtes Kalenderelement an.
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465310"
---
# <a name="range"></a>Bereich

Das **Range** -Element gibt einen Bereich von Kalenderelement Vorkommen für ein wiederholtes Kalenderelement an. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Start** <br/> |Der Textwert des **Start** -Attributs entspricht dem Startdatum des Bereichs für wiederkehrende Elemente. Dies ist ein **DateTime** -Wert.  <br/> |
|**End** <br/> |Der Textwert des **End** -Attributs entspricht dem Enddatum des Bereichs für wiederkehrende Elemente. Dies ist ein **DateTime** -Wert.  <br/> |
|**Count** <br/> |Der Textwert des **count** -Attributs ist die Anzahl der Vorkommen des wiederkehrenden Elements. Dies ist ein **ganzzahliger** Wert.  <br/> |
|**CompareOriginalStartTime** <br/> |Der Textwert **true** für das **CompareOriginalStartTime** -Attribut gibt an, dass der Client die ursprüngliche Startzeit mit der neuen Startzeit vergleichen sollte. Der Wert **false** gibt an, dass der Client die ursprüngliche Anfangszeit nicht mit der neuen Startzeit vergleichen muss.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Ranges](ranges.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

