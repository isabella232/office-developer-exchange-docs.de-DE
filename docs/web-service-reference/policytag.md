---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: Das PolicyTag-Element gibt den Aufbewahrungsbezeichner für ein Element oder einen Ordner an.
ms.openlocfilehash: 16759748dded6978e68450a6b8d504dd378c04be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519254"
---
# <a name="policytag"></a>PolicyTag

Das **PolicyTag-Element** gibt den Aufbewahrungsbezeichner für ein Element oder einen Ordner an. 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 **RetentionTagType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|IsExplicit  <br/> |Gibt an, ob ein Richtlinientag explizit für ein Element oder einen Ordner festgelegt wurde.  <br/> Der Textwert **"true"** für das **IsExplicit-Attribut** gibt an, dass das Richtlinientag explizit für das Element oder den Ordner festgelegt wurde. Der Textwert **"false"** gibt an, dass das Richtlinientag implizit für das Element oder den Ordner basierend auf dem übergeordneten Ordnerrichtlinientag festgelegt wurde.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchPreviewItem](searchpreviewitem.md)  |  [Element](item.md)  |  [Kontakt](contact.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **PolicyTag-Elements** ist der Richtlinientagbezeichner. Der Richtlinientagbezeichner ist eine GUID. 
  
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
   

