---
title: IsUndecidedApprovalRequest
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90841617-3b83-4124-8125-0293c9470f4a
description: Das IsUndecidedApprovalRequest-Element gibt an, ob eine Genehmigung Request-Nachricht auf gefasst.
ms.openlocfilehash: 82b4624df5b2fe7ca212fdf76248e1ccfa3a081f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830127"
---
# <a name="isundecidedapprovalrequest"></a>IsUndecidedApprovalRequest

Das **IsUndecidedApprovalRequest** -Element gibt an, ob eine Genehmigung Request-Nachricht auf gefasst. 
  
```XML
<IsUndecidedApprovalRequest> true | false </IsUndecidedApprovalRequest>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ApprovalRequestData](approvalrequestdata.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **IsUndecidedApprovalRequest** -Element ist **true** , wenn eine Genehmigung Request-Nachricht nicht auf tätig geworden ist. Der Wert **false** gibt an, dass die genehmigungsanforderung festgelegt wurde. 
  
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



[ApprovalRequestData](approvalrequestdata.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

