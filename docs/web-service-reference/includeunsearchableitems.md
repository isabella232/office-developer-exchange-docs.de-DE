---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: Das IncludeUnsearchableItems-Element gibt an, ob Elemente eingeschlossen werden sollen, die nicht durchsucht werden können.
ms.openlocfilehash: 3bffd68c20623aa4c63dd295d8b4619999c1d4a5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533104"
---
# <a name="includeunsearchableitems"></a>IncludeUnsearchableItems

Das **IncludeUnsearchableItems-Element** gibt an, ob Elemente eingeschlossen werden sollen, die nicht durchsucht werden können. 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindMailboxStatisticsByKeywords](findmailboxstatisticsbykeywords.md) <br/> |Gibt eine Anforderung an, nach Postfachstatistiken nach Schlüsselwort zu suchen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IncludeUnsearchableItems-Element** gibt an, dass keine Statistiken für Elemente enthalten sind, die nicht durchsuchbar sind. Der Wert **"false"** gibt an, dass Statistiken für Elemente enthalten sind, die nicht durchsuchbar sind. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

