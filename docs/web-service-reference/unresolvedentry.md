---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: Das UnresolvedEntry-Element enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll.
ms.openlocfilehash: 0f157c1be6c327187456a795c4c1000b8c35b620
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459840"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

Das **UnresolvedEntry** -Element enthält den Namen eines Kontakts oder einer Verteilerliste, die aufgelöst werden soll. 
  
[ResolveNames](resolvenames.md)
  
[UnresolvedEntry](unresolvedentry.md)
  
```xml
<UnresolvedEntry/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResolveNames](resolvenames.md) <br/> |Definiert eine Anforderung zum Auflösen eindeutiger Namen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt den Namen eines öffentlichen Kontakts oder einer Verteilerliste dar. Die minimale Länge der Zeichenfolge ist ein Zeichen.
  
## <a name="remarks"></a>Bemerkungen

Der Textwert dieses Elements wird zum Auflösen von Namen in den folgenden Feldern verwendet:
  
- Vorname
    
- Nachname
    
- Distinguished Name (DN)
    
- Vollständiger Name
    
- Office
    
- Alias
    
- SMTP-Adresse
    
E-Mail-Adressen mit vorfixierten Routing Typen wie SMTP oder SIP werden in einem mehrwertigen Array gespeichert. Der [ResolveNames-Vorgang](resolvenames-operation.md) führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten namens hinzufügen, beispielsweise "SIP:user1@contoso.com". Wenn Sie keinen Routingtyp angeben, wird der **ResolveNames** -Vorgang standardmäßig auf den Routingtyp von SMTP festgelegt, mit einer primären SMTP-Adress Eigenschaft abgeglichen und nicht mit dem mehrwertigen Array durchsucht. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

