---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: Das VotingInformation-Element gibt Abstimmungsinformationen zu einer Abstimmungsnachricht und einer Genehmigungsanforderungsnachricht an, wobeiApproveandReject die Abstimmungsoptionen sind.
ms.openlocfilehash: 7e5aedddbfe97bba935aa56b3583e2fb8b081320
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543856"
---
# <a name="votinginformation"></a>VotingInformation

Das **VotingInformation-Element** gibt Abstimmungsinformationen zu einer Abstimmungsnachricht und einer Genehmigungsanforderungsnachricht an, wobei "Genehmigen" und "Ablehnen" die Abstimmungsoptionen sind. 
  
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

[UserOptions](useroptions.md)  |  [VotingResponse](votingresponse.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Meldung](message-ex15websvcsotherref.md)
  
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



[Meldung](message-ex15websvcsotherref.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

