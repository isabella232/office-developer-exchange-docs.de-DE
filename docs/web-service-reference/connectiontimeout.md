---
title: ConnectionTimeout
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConnectionTimeout
api_type:
- schema
ms.assetid: 14da68a0-bcca-4281-a774-47644baa4ee9
description: Das ConnectionTimeout-Element gibt die Anzahl der Minuten an, die eine Verbindung geöffnet bleiben soll.
ms.openlocfilehash: 671e3cf5466ee8b3543036811708bd7f54afdcce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463853"
---
# <a name="connectiontimeout"></a>ConnectionTimeout

Das **ConnectionTimeout** -Element gibt die Anzahl der Minuten an, die eine Verbindung geöffnet bleiben soll. 
  
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
|[GetStreamingEvents](getstreamingevents.md) <br/> |Definiert eine Anforderung zum Abrufen von Ereignisbenachrichtigungen aus einer streamingverbindung.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine ganze Zahl dar, die die maximale Anzahl von Minuten beschreibt, die eine streamingverbindung geöffnet bleiben soll. Der Wert muss zwischen 1 und 30 einschließlich sein.
  
## <a name="remarks"></a>Bemerkungen

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

