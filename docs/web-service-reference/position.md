---
title: Position
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 46726ebb-a403-4793-8378-282aa7dc39d0
description: Das Position-Element gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde.
ms.openlocfilehash: 6b4e7c12bbcf12b8804619caa508f5c2c0bc4eda
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515292"
---
# <a name="position"></a>Position

Das **Position-Element** gibt die Position einer Entität an, die aus einer Nachricht extrahiert wurde. 
  
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

[UrlEntity](urlentity.md)  |  [AddressEntity](addressentity.md)  |  [EmailAddressEntity](emailaddressentity.md)  |  [MeetingSuggestion](meetingsuggestion.md)  |  [Kontakt (ContactType)](contact-contacttype.md)  |  [Telefon (PhoneEntityType)](phone-phoneentitytype.md)  |  [TaskSuggestion](tasksuggestion.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des Position-Elements ist der Speicherort, an dem eine extrahierte Entität aus der Quellnachricht stammt.  Die Textwerte für das **Position-Element** sind: 
  
- **LatestReply** – die extrahierte Entität stammt aus der letzten Antwort auf die Nachricht. 
    
- **Andere** : Die extrahierte Entität stammt aus einem nicht definierten Teil der Nachricht. 
    
- **Betreff** : Die extrahierte Entität stammt aus dem Nachrichtenbetreff. 
    
- **Signatur** – die extrahierte Entität stammt aus der Nachrichtensignatur. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

