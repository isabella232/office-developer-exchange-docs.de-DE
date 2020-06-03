---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: Das GlobalHasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist.
ms.openlocfilehash: 10b99c9a6421a89a549b69e918087f3e542ffa09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459469"
---
# <a name="globalhasirm"></a>GlobalHasIrm

Das **GlobalHasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist. 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **GlobalHasIrm** -Elements ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützte Nachricht ist. Andernfalls ist der Wert **false**.
  
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



[Unterhaltung (ConversationType)](conversation-conversationtype.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

