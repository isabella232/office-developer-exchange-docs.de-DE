---
title: TimeZoneContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZoneContext
api_type:
- schema
ms.assetid: 573c462b-aa1d-4ba0-8852-e3f48b26873b
description: Das TimeZoneContext-Element wird im SOAP-Header (Simple Object Access Protocol) verwendet, um die Zeitzonendefinition anzugeben, die als Standard verwendet werden soll, wenn die Zeitzone für die DateTime-Eigenschaften von Objekten zugewiesen wird, die mit Exchange Webdienste (EWS) erstellt, aktualisiert und abgerufen werden.
ms.openlocfilehash: a628d4a094e70f1190f2cc0eda8cc4416bc37860
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515173"
---
# <a name="timezonecontext"></a>TimeZoneContext

Das **TimeZoneContext-Element** wird im SOAP-Header (Simple Object Access Protocol) verwendet, um die Zeitzonendefinition anzugeben, die als Standard verwendet werden soll, wenn die Zeitzone für die DateTime-Eigenschaften von Objekten zugewiesen wird, die mithilfe von Exchange Webdienste (EWS) erstellt, aktualisiert und abgerufen werden. 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 **TimeZoneContextType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Gibt die Zeiträume und Übergänge an, die eine Zeitzone definieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

