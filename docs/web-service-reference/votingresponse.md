---
title: VotingResponse
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7dae4db5-28d3-4b81-b071-458c814c36b9
description: Das VotingResponse-Element gibt gesendete stimmen. Dieses Element ist nur für Antworten auf Abstimmungsoptionen Anforderungsnachrichten, nicht für Antworten auf Genehmigungen vorhanden.
ms.openlocfilehash: 865b24a4f7ec1cc7b53d4928b04f071cddf5fbfc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839508"
---
# <a name="votingresponse"></a>VotingResponse

Das **VotingResponse** -Element gibt gesendete stimmen. Dieses Element ist nur für Antworten auf Abstimmungsoptionen Anforderungsnachrichten, nicht für Antworten auf Genehmigungen vorhanden. 
  
```XML
<VotingResponse />
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[VotingInformation](votinginformation.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **VotingResponse** -Element ist der Abstimmung übermittelt. 
  
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



[VotingInformation](votinginformation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

