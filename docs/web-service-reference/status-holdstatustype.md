---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Das Status-Element gibt den Haltestatus für ein Postfach an.
ms.openlocfilehash: a055dde61ae52c266f2349036c881d2b00557171
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521235"
---
# <a name="status-holdstatustype"></a>Status (HoldStatusType)

Das **Status-Element** gibt den Haltestatus für ein Postfach an. 
  
```XML
<Status> NotOnHold | Pending | OnHold | PartialHold | Failed </Status>
```

 **HoldStatusType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MailboxHoldStatus](mailboxholdstatus.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Status-Elements** ist der Haltestatus eines Postfachs. Das **Status-Element** kann die Werte in der folgenden Liste enthalten. 
  
> NotOnHold: Das Postfach ist nicht in der Warteschleife.
    
> Ausstehend – Das Postfach steht aus, entweder wird in die Warteschleife gestellt oder freigegeben. 
    
> OnHold : Die Aufbewahrung wurde erfolgreich auf das Postfach angewendet. 
    
> PartialHold : Die Aufbewahrung wurde erfolgreich auf einige Postfächer, aber nicht auf alle Postfächer angewendet.
    
> Fehlgeschlagen– Die Aufbewahrung konnte nicht auf das Postfach angewendet werden.
    
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

