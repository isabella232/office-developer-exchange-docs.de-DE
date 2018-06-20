---
title: StartTimeZoneId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4adfc48-2d51-4d2d-9ddc-b91c3e96cb02
description: Das StartTimeZoneId-Element gibt die Zeitzone an, in dem eine Besprechung erfolgt.
ms.openlocfilehash: d131a4cad3076c1ed4044dbcbe49f1dfa4ed5ccf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831567"
---
# <a name="starttimezoneid"></a>StartTimeZoneId

Das **StartTimeZoneId** -Element gibt die Zeitzone an, in dem eine Besprechung erfolgt. 
  
```XML
<StartTimeZoneId></StartTimeZoneId>
```

**string**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[CalendarItem](calendaritem.md) | [MeetingRequest](meetingrequest.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **StartTimeZoneId** -Elements ist die Zeitzonenbezeichner der Zeitzone, die in der [Start](start.md) -Element verwendet. 
  
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
   

