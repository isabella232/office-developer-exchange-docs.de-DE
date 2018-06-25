---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: Das PolicyTag-Element gibt den Bezeichner für die Aufbewahrung auf eines Elements oder Ordners.
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830835"
---
# <a name="policytag"></a>PolicyTag

Das **PolicyTag** -Element gibt den Bezeichner für die Aufbewahrung auf eines Elements oder Ordners. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|IsExplicit  <br/> |Gibt an, ob ein Tag Richtlinie auf eines Elements oder Ordners explizit festgelegt wurde.  <br/> Der Textwert **true** für das **IsExplicit** -Attribut gibt an, dass das Tag Richtlinie auf des Elements oder Ordners explizit festgelegt wurde. Der Textwert **false** gibt an, dass das Tag Richtlinie implizit für des Elements oder Ordners basierend auf dem übergeordneten Ordner Policy Tag festgelegt wurde.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchPreviewItem](searchpreviewitem.md) | [Element](item.md) | [Kontakt](contact.md) | [Nachricht](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **PolicyTag** -Elements ist die Richtlinie Tag-Bezeichner. Die Richtlinie Tag-ID ist eine GUID. 
  
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
   

