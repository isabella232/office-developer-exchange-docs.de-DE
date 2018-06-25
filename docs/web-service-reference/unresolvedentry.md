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
description: Das UnresolvedEntry-Element enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben.
ms.openlocfilehash: 98b447cd49685b49f73f75f12d921a65749be245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839324"
---
# <a name="unresolvedentry"></a>UnresolvedEntry

Das **UnresolvedEntry** -Element enthält den Namen des einen Kontakt oder Verteilerliste aus, zu beheben. 
  
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
|[ResolveNames](resolvenames.md) <br/> |Definiert eine Anforderung zum Auflösen von Names nicht eindeutig.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt den Namen einer öffentlichen Liste Kontakts oder der Verteilergruppe. Die minimale Länge der Zeichenfolge ist ein Zeichen.
  
## <a name="remarks"></a>Hinweise

Der Textwert der dieses Element dient zum Auflösen von Namen für die folgenden Felder:
  
- Vorname
    
- Nachname
    
- Anzeigename
    
- Vollständiger name
    
- Office
    
- Alias
    
- SMTP-Adresse
    
E-Mail-Adressen mit vorangestellter routing Typen, wie die SMTP- oder Sip, werden in einem mehrwertigen Array gespeichert. Den [ResolveNames Vorgang](resolvenames-operation.md) ausführt eine teilweise Übereinstimmung mit jeder Wert eines Arrays aus, wenn Sie den Routingtyp am Anfang der aufgelöste Name, beispielsweise "sip:User1@Contoso.com" hinzufügen. Wenn Sie eine Routingtyp nicht angeben, wird **ResolveNames** -Vorgang standardmäßig auf den Routingtyp von smtp, es zu einer primären SMTP-Adresse-Eigenschaft entspricht und nicht durchsucht das mehrwertige Array. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ResolveNames-Vorgang](resolvenames-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

