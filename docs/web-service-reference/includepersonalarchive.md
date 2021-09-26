---
title: IncludePersonalArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b373bb1a-6b1d-4959-98a1-4c4ea62973bc
description: Das IncludePersonalArchive-Element gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll.
ms.openlocfilehash: 2567475fbb2542c7d01e651f2d348f6f91d50b78
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547218"
---
# <a name="includepersonalarchive"></a>IncludePersonalArchive

Das **IncludePersonalArchive-Element** gibt an, ob das persönliche Archiv in die Suche einbezogen werden soll. 
  
```XML
<IncludePersonalArchive>true | false</IncludePersonalArchive>
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

Der Textwert **"true"** für das **IncludePersonalArchive-Element** gibt an, dass das persönliche Archiv in der Suche enthalten ist. Der Wert **"false"** gibt an, dass das persönliche Archiv nicht in der Suche enthalten ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

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

