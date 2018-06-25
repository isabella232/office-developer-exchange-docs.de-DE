---
title: Range
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Range-Element gibt einen Bereich von Kalender Element Vorkommen eines Serienelements Kalender.
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830946"
---
# <a name="range"></a>Range

**Range** -Element gibt einen Bereich von Kalender Element Vorkommen eines Serienelements Kalender. 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Start** <br/> |Der Textwert der **Start** -Attribut ist das Startdatum des sich wiederholenden Bereich. Dies ist ein **DateTime** -Wert.  <br/> |
|**End** <br/> |Der Textwert der **End** -Attribut wird das Enddatum des Bereichs sich wiederholenden Element. Dies ist ein **DateTime** -Wert.  <br/> |
|**Count** <br/> |Der Textwert der **Count** -Attribut ist die Anzahl der Vorkommen eines wiederkehrenden Objekts. Dies ist eine **ganze** Zahl.  <br/> |
|**CompareOriginalStartTime** <br/> |Der Textwert der **"true"** für das **CompareOriginalStartTime** -Attribut gibt an, dass der Client die ursprüngliche Startzeit mit den neuen Startzeit verglichen werden soll. Der Wert **false** gibt an, dass der Client nicht notwendigerweise die ursprünglichen Startzeit mit den neuen Startzeit verglichen werden soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Ranges](ranges.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

