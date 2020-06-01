---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: Das VotingResponse-Element gibt die übermittelte Abstimmung an. Dieses Element ist nur bei Antworten auf Abstimmungs Anforderungsnachrichten vorhanden, nicht bei Antworten auf Genehmigungen.
ms.openlocfilehash: ed7caff79d1ff2946800630c167350fe866e29dc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466465"
---
# <a name="votingresponse"></a>VotingResponse

Das **VotingResponse** -Element gibt die übermittelte Abstimmung an. Dieses Element ist nur bei Antworten auf Abstimmungs Anforderungsnachrichten vorhanden, nicht bei Antworten auf Genehmigungen. 
  
```XML
<VotingResponse />
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[VotingInformation](votinginformation.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **VotingResponse** -Elements ist die abgegebene Stimme. 
  
## <a name="remarks"></a>Bemerkungen

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



[VotingInformation](votinginformation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

