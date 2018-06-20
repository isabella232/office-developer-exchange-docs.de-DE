---
title: SendPrompt
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22cb5a30-75d9-49a8-9d98-255f2e8a722d
description: Das SendPrompt-Element gibt den Typ der Aktion für ein voting Option zulässig.
ms.openlocfilehash: f3220d957482ea04c46b014cdf1c67025d5ec21a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831346"
---
# <a name="sendprompt"></a>SendPrompt

Das **SendPrompt** -Element gibt den Typ der Aktion für ein voting Option zulässig. 
  
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

Der Textwert des **SendPrompt** -Elements ist eine voting Option Aktion. Die folgende Tabelle enthält die möglichen Werte für dieses Element. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Keine  <br/> |Keine Aktion.  <br/> |
|Senden  <br/> |Die Antwort wird sofort gesendet.  <br/> |
|VotingOption  <br/> |Die genehmigende Person kann Eincheckkommentare beim Genehmigen oder ablehnen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[VotingOptionData](votingoptiondata.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

