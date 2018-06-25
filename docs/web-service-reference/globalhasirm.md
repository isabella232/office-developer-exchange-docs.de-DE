---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: Das GlobalHasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist.
ms.openlocfilehash: ad3eafcb38829e7ea57cbc7535b0f5411ad595d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829717"
---
# <a name="globalhasirm"></a>GlobalHasIrm

Das **GlobalHasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist. 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **GlobalHasIrm** -Element ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und in allen Ordnern eine IRM-geschützten Nachricht ist. Andernfalls ist der Wert **false**.
  
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



[Unterhaltung (ConversationType)](conversation-conversationtype.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

