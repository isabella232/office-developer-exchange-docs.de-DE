---
title: UnresolvedEntry
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UnresolvedEntry
api_type:
- schema
ms.assetid: 5ac6116a-3b24-40f8-a877-dbe9a6935919
description: Das UnresolvedEntry-Element enthält den Namen eines Kontakts oder einer Verteilerliste, der aufgelöst werden soll.
ms.openlocfilehash: 77074d5aed0a799d355fd176a8c9c06f2dffec5a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538667"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

Das **UnresolvedEntry-Element** enthält den Namen eines Kontakts oder einer Verteilerliste, der aufgelöst werden soll. 
  
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
|[ResolveNames](resolvenames.md) <br/> |Definiert eine Anforderung zum Auflösen von mehrdeutigen Namen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Namen eines öffentlichen Kontakts oder einer Verteilerliste dar. Die Mindestlänge der Zeichenfolge beträgt ein Zeichen.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Textwert dieses Elements wird verwendet, um Namen in den folgenden Feldern aufzulösen:
  
- Vorname
    
- Nachname
    
- Anzeigename
    
- Vollständiger Name
    
- Office
    
- Alias
    
- SMTP-Adresse
    
E-Mail-Adressen mit Routingtypen mit Präfix, z. B. SMTP oder SIP, werden in einem mehrwertigen Array gespeichert. Der [ResolveNames-Vorgang](resolvenames-operation.md) führt eine partielle Übereinstimmung mit jedem Wert dieses Arrays aus, wenn Sie den Routingtyp am Anfang des nicht aufgelösten Namens hinzufügen, z. B. "sip:User1@Contoso.com". Wenn Sie keinen Routingtyp angeben, wird der **ResolveNames-Vorgang** standardmäßig auf den Routingtyp von SMTP festgelegt, mit einer primären SMTP-Adresseigenschaft abgeglichen und das mehrwertige Array nicht durchsucht. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

