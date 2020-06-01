---
title: ErrorCode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0bb00cee-c66b-4f34-b99d-355458f5e83b
description: Das ErrorCode-Element stellt einen Fehlercode für die Regelüberprüfung dar, der beschreibt, welche fehlgeschlagene Validierung für jedes Regelprädikat oder jede Aktion ausgeführt wurde.
ms.openlocfilehash: 6432aeee786d74a9afcb346cb66765f9001257de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460078"
---
# <a name="errorcode"></a>ErrorCode

Das **errorCode** -Element stellt einen Fehlercode für die Regelüberprüfung dar, der beschreibt, welche fehlgeschlagene Validierung für jedes Regelprädikat oder jede Aktion ausgeführt wurde. 
  
```XML
<ErrorCode/>
```

 **RuleValidationErrorCodeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Fehler](error.md) <br/> |Stellt einen einzelnen Validierungsfehler für einen bestimmten Regel Eigenschaftswert, einen Prädikateigenschaftswert oder einen Action-Eigenschaftswert dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert für dieses Element ist auf eine der folgenden Zeichenfolgen beschränkt:
  
- ADOperationFailure
    
- ConnectedAccountNotFound
    
- CreateWithRuleId
    
- EmptyValueFound
    
- DuplicatedPriority
    
- DuplicatedOperationOnTheSameRule
    
- FolderDoesNotExist
    
- InvalidAddress
    
- InvalidDateRange
    
- InvalidFolderId
    
- InvalidSizeRange
    
- Invalidvalue
    
- MessageClassificationNotFound
    
- Missing
    
- Missparameter
    
- MissingRangeValue
    
- NotSettable
    
- RecipientDoesNotExist
    
- RuleNotFound
    
- SizeLessThanZero
    
- StringValueTooBig
    
- UnsupportedAddress
    
- UnexpectedError
    
- UnsupportedRule
    
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

