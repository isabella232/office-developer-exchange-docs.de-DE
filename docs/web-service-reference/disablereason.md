---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: Das DisableReason-Element gibt den Grund für die Deaktivierung einer app.
ms.openlocfilehash: f900bd1b98b294900f767c778b9c5f87f74042ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758011"
---
# <a name="disablereason"></a>DisableReason

Das **DisableReason** -Element gibt den Grund für die Deaktivierung einer app. 
  
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
|[DisableApp](disableapp.md) <br/> |Gibt eine Anforderung an eine app zu deaktivieren.  <br/> |
   
## <a name="text-value"></a>Textwert

**DisableReason Elementwert text**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NoReason  <br/> |Kein Grund angegeben  <br/> |
|OutlookClientPerformance  <br/> |Zum Verbessern der Leistung der e-Mail-Client.  <br/> |
|OWAClientPerformance  <br/> |Zur Verbesserung der Leistung von Web app-Client.  <br/> |
|MobileClientPerformance  <br/> |Zum Verbessern der Leistung von mobilen Clients.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

