---
title: IsAutomaticForward
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAutomaticForward
api_type:
- schema
ms.assetid: 6876b849-a648-482e-8934-93eb5a0c465f
description: Das IsAutomaticForward-Element gibt an, ob eingehende Nachrichten automatische Weiterleitungen in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen.
ms.openlocfilehash: c2d44d6dce30cbf55e0c7673aaf41b114a3e2cd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829989"
---
# <a name="isautomaticforward"></a>IsAutomaticForward

Das **IsAutomaticForward** -Element gibt an, ob eingehende Nachrichten automatische Weiterleitungen in Reihenfolge für die Bedingung oder Ausnahme angewendet werden müssen. 
  
```XML
<IsAutomaticForward/> true | false</IsAutomaticForward>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass die Nachricht eine automatische Weiterleitung in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss. Der Wert **false** gibt an, dass die Nachricht keine automatische Weiterleitung in der Reihenfolge für die Bedingung oder Ausnahme angewendet werden muss. 
  
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



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

