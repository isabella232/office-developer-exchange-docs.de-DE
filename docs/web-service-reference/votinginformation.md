---
title: VotingInformation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 351c8dfe-cf8c-45ba-a07d-d764f8189773
description: Das VotingInformation-Element gibt die Abstimmungsoptionen voting Informationen für eine Nachricht Abstimmungsoptionen und Genehmigung Anforderung Nachricht WhereApproveandRejectare.
ms.openlocfilehash: f11c25bb1f3a3c4781cfa6c51e11ff87af40c7f0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839502"
---
# <a name="votinginformation"></a>VotingInformation

Das **VotingInformation** -Element gibt voting Informationen für eine Nachricht Abstimmungsoptionen und Genehmigung Request-Nachricht, wobei "Genehmigen" und "Ablehnen" die Abstimmungsoptionen sind. 
  
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

[UserOptions](useroptions.md) | [VotingResponse](votingresponse.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Message](message-ex15websvcsotherref.md)
  
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



[Message](message-ex15websvcsotherref.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

