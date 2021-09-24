---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: Das IsUndecidedApprovalRequest-Element gibt an, ob eine Genehmigungsanforderungsnachricht ausgeführt wurde.
ms.openlocfilehash: 5204793490015bd2999322c0f029445c7df91e02
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511413"
---
# <a name="isundecidedapprovalrequest"></a>IsUndecidedApprovalRequest

Das **IsUndecidedApprovalRequest-Element** gibt an, ob eine Genehmigungsanforderungsnachricht ausgeführt wurde. 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **IsUndecidedApprovalRequest-Elements** ist **"true",** wenn eine Genehmigungsanforderungsnachricht nicht behandelt wurde. Der Wert **"false"** gibt an, dass die Genehmigungsanforderung entschieden wurde. 
  
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



[ApprovalRequestData](approvalrequestdata.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

