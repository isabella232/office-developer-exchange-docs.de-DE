---
title: ProcessRightAway
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ProcessRightAway
api_type:
- schema
ms.assetid: f6bba68b-ae4f-41c1-b3e7-c8a31cdb1b0c
description: Das ProcessRightAway-Element gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann.
ms.openlocfilehash: 58d2b926c48db5e7395df64e1f8ee9d6a8f0e73c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44434071"
---
# <a name="processrightaway"></a>ProcessRightAway

Das **ProcessRightAway** -Element gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[Unterhaltung](conversationaction.md)
  
[ProcessRightAway](processrightaway.md)
  
```XML
<ProcessRightAway/>
```

 **xs: Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung](conversationaction.md) <br/> |Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird. Der Textwert **false** gibt an, dass die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

