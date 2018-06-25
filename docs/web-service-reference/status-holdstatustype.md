---
title: Status (HoldStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fee3f1f9-e868-49fa-a554-7ff096964718
description: Status-Element gibt den Sperrstatus für ein Postfach an.
ms.openlocfilehash: c40dc865d2b305ac86fa40d536e2d516a14260ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831579"
---
# <a name="status-holdstatustype"></a>Status (HoldStatusType)

**Status** -Element gibt den Sperrstatus für ein Postfach an. 
  
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

Der Textwert der **Status** -Element wird der Sperrstatus eines Postfachs an. **Status** -Element kann die Werte in der folgenden Liste haben. 
  
> NotOnHold - ist das Postfach nicht in der Warteschleife.
    
> Ausstehende - wurde das Postfach entweder platziert oder in der Warteschleife veröffentlicht wird. 
    
> Vortext - Haltebereich wurde erfolgreich an das Postfach angewendet. 
    
> PartialHold - Haltebereich wurde erfolgreich für Postfächer, jedoch nicht für alle Postfächer angewendet.
    
> Fehler bei - konnte der Haltestatus an das Postfach anwenden.
    
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

