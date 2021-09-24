---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: Das DisableReason-Element gibt den Grund für das Deaktivieren einer App an.
ms.openlocfilehash: 8156dac17e81dd1c3f49575491924185b04d53e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528836"
---
# <a name="disablereason"></a>DisableReason

Das **DisableReason-Element** gibt den Grund für das Deaktivieren einer App an. 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 **DisableReasonType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DisableApp](disableapp.md) <br/> |Gibt eine Anforderung zum Deaktivieren einer App an.  <br/> |
   
## <a name="text-value"></a>Textwert

**DisableReason-Elementtextwert**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NoReason  <br/> |Kein Grund angegeben  <br/> |
|OutlookClientPerformance  <br/> |Um die Leistung des E-Mail-Clients zu verbessern.  <br/> |
|OWAClientPerformance  <br/> |Um die Leistung des Web App-Clients zu verbessern.  <br/> |
|MobileClientPerformance  <br/> |Zur Verbesserung der Leistung mobiler Clients.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

