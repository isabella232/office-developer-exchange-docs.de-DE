---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Das Position-Element gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde.
ms.openlocfilehash: 9acd965c3e0c29f3fa91df338c0671749192b38b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465422"
---
# <a name="position"></a>Position

Das **Position** -Element gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde. 
  
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

[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Kontakt (ContactType)](contact-contacttype.md)  |  [Telefon (PhoneEntityType)](phone-phoneentitytype.md)  |  [Task Suggestion](tasksuggestion.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Position** -Elements ist die Position, an der eine extrahierte Entität in der Quellnachricht stammt. Die Textwerte für das **Position** -Element lauten wie folgt: 
  
- **LatestReply** – die extrahierte Entität stammt aus der letzten Antwort auf die Nachricht. 
    
- **Other** -die extrahierte Entität stammt aus einem nicht definierten Teil der Nachricht. 
    
- **Betreff** – die extrahierte Entität stammt aus dem Nachrichtenbetreff. 
    
- **Signatur** – die extrahierte Entität stammt aus der Nachrichtensignatur. 
    
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

