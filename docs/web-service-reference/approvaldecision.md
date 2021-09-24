---
title: ApprovalDecision
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5e7c5687-cb9e-4f0b-ac8f-b82591914a39
description: Das ApprovalDecision-Element gibt die Entscheidung an, die in einer Genehmigungsanforderungsnachricht getroffen wurde.
ms.openlocfilehash: 903b75f04255a19ebb7a9b4d0e47b685f22d4339
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517231"
---
# <a name="approvaldecision"></a>ApprovalDecision

Das **ApprovalDecision-Element** gibt die Entscheidung an, die in einer Genehmigungsanforderungsnachricht getroffen wurde. 
  
```XML
<ApprovalDecision> 1 | 2 </ApprovalDecision>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **ApprovalDecision-Elements** ist 1, wenn genehmigt, und 2, wenn abgelehnt. 
  
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

- [ApprovalRequestData](approvalrequestdata.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

