---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: Das SendPrompt-Element gibt den Typ der Aktion an, die für eine Abstimmungsoption zulässig ist.
ms.openlocfilehash: 32537210aadce91911d1fb5002fbafcaa70aa9ab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532132"
---
# <a name="sendprompt"></a>SendPrompt

Das **SendPrompt-Element** gibt den Typ der Aktion an, die für eine Abstimmungsoption zulässig ist. 
  
```XML
<SendPrompt> None | Send | VotingOption </SendPrompt>
```

 **SendPromptType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[VotingOptionData](votingoptiondata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SendPrompt-Elements** ist eine Abstimmungsoptionsaktion. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Keine Aktion.  <br/> |
|Senden  <br/> |Die Antwort wird sofort gesendet.  <br/> |
|VotingOption  <br/> |Die genehmigende Person kann kommentare eingeben, während sie genehmigt oder abgelehnt wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[VotingOptionData](votingoptiondata.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

