---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: Das PolicyTag-Element gibt die Aufbewahrungs-ID für ein Element oder einen Ordner an.
ms.openlocfilehash: ddc4d890d1e514586ba5ea7f6a8b541b2e4786c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460897"
---
# <a name="policytag"></a>PolicyTag

Das **PolicyTag** -Element gibt die Aufbewahrungs-ID für ein Element oder einen Ordner an. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Isexplicit  <br/> |Gibt an, ob ein Richtlinien Tag explizit für ein Element oder einen Ordner festgelegt wurde.  <br/> Der Textwert **true** für das Attribut **isexplicit** gibt an, dass das richtlinientag explizit für das Element oder den Ordner festgelegt wurde. Der Textwert **false** gibt an, dass das richtlinientag für das Element oder den Ordner basierend auf dem richtlinientag des übergeordneten Ordners implizit festgelegt wurde.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchPreviewItem](searchpreviewitem.md)  |  [Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [Verteilerliste](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **PolicyTag** -Elements ist der Bezeichner des Richtlinien Tags. Der Bezeichner des Richtlinien Tags ist eine GUID. 
  
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
   

