---
title: StopProcessingRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StopProcessingRules
api_type:
- schema
ms.assetid: 5b89a2cb-ab26-444d-b3dd-2b3858872d63
description: Das StopProcessingRules -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll.
ms.openlocfilehash: 48799975f8c928bf291fcdcdb83f2ff8768af8b9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831593"
---
# <a name="stopprocessingrules"></a>StopProcessingRules

Das **StopProcessingRules** -Element gibt an, ob nachfolgende Regeln sind ausgewertet werden soll. 
  
```XML
<StopProcessingRules>true | false</StopProcessingRules>
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
|[Aktionen](actions.md) <br/> |Repräsentiert den Satz von Aktionen, die sind verfügbar, die auf eine Nachricht durchgeführt werden, wenn die Bedingungen erfüllt sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass nachfolgende Regeln nicht verarbeitet werden soll. Der Wert **false** gibt an, dass nachfolgende Regeln ausgewertet wird fortgesetzt werden soll. 
  
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

