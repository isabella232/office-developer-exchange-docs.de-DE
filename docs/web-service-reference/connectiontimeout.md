---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: Das ConnectionTimeout-Element gibt die Anzahl der Minuten an, um eine Verbindung geöffnet zu lassen.
ms.openlocfilehash: 7ca7a0b0b71d40a4f7888b63663b7d1e0f81b449
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536827"
---
# <a name="connectiontimeout"></a>ConnectionTimeout

Das **ConnectionTimeout-Element** gibt die Anzahl der Minuten an, um eine Verbindung geöffnet zu lassen. 
  
[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)
  
[ConnectionTimeout](connectiontimeout.md)
  
```xml
<ConnectionTimeout/>
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
|[GetStreamingEvents](getstreamingevents.md) <br/> |Definiert eine Anforderung zum Abrufen von Ereignisbenachrichtigungen von einer Streamingverbindung.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine ganze Zahl dar, die die maximale Anzahl von Minuten beschreibt, um eine Streamingverbindung geöffnet zu lassen. Der Wert muss zwischen 1 und 30 (einschließlich) liegen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

