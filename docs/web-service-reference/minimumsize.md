---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: Das Element MinimumSize stellt die Mindestgröße, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss.
ms.openlocfilehash: 4f80bac3b9226019ec3d726cd2d6430e02cac423
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830480"
---
# <a name="minimumsize"></a>MinimumSize

Das Element **MinimumSize** stellt die Mindestgröße, die eine Nachricht in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss. 
  
```XML
<MinimumSize/>
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
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die minimale und maximale Größe, die eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die die minimale Größe der Nachricht in Bytes angibt.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Max](maximumsize.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

