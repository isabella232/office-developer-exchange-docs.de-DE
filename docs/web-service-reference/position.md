---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Das Position-Element gibt die Position einer Entität aus einer Nachricht extrahiert haben.
ms.openlocfilehash: 4bd8f3088891e918e13d5ef1ec8e3e5217cb3fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830853"
---
# <a name="position"></a>Position

Das **Position** -Element gibt die Position einer Entität aus einer Nachricht extrahiert haben. 
  
```XML
<Position> LatestReply | Other | Subject | Signature </Position>
```

 **EmailPositionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[UrlEntity](urlentity.md) | [AddressEntity](addressentity.md) | [EmailAddressEntity](emailaddressentity.md) | [MeetingSuggestion](meetingsuggestion.md) | [Kontakt (Kontakttyp den)](contact-contacttype.md) | [Phone (PhoneEntityType)](phone-phoneentitytype.md)  |  [ TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Position** -Elements ist der Speicherort, von dem eine extrahierte Entität in der Quellnachricht stammt. Die Textwerte für das Element **Position** sind: 
  
- **LatestReply** - die extrahierte Entität stammt aus der neuesten Antwort auf die Meldung. 
    
- **Andere** - die extrahierte Entität stammt aus einem nicht definierten Teil der Nachricht. 
    
- **Betreff** - die extrahierte Entität stammt aus der Betreff der Nachricht. 
    
- **Signatur** - die extrahierte Entität stammt aus der Nachrichtensignatur. 
    
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

