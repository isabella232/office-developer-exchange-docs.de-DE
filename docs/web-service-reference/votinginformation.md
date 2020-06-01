---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: Das VotingInformation-Element gibt Abstimmungsinformationen in einer Abstimmungs Nachricht und einer Genehmigungs Anforderungsnachricht whereApproveandRejectare den Abstimmungsoptionen an.
ms.openlocfilehash: d946ba8c71d19c8cbb1befbe8c4e43e93590ccae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44467746"
---
# <a name="votinginformation"></a>VotingInformation

Das **VotingInformation** -Element gibt Abstimmungsinformationen in einer Abstimmungs Nachricht und einer Genehmigungs Anforderungsnachricht an, wobei "genehmigen" und "ablehnen" die Abstimmungsoptionen sind. 
  
```XML
<VotingInformation
   <UserOptions/>
   <VotingResponse/>
</VotingInformation>
```

 **VotingInformationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[USEROPTIONS](useroptions.md)  |  [VotingResponse](votingresponse.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Nachricht](message-ex15websvcsotherref.md)
  
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



[Nachricht](message-ex15websvcsotherref.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

