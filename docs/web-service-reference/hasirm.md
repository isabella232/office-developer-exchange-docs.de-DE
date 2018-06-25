---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: Das HasIrm-Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und der aktuelle Ordner ein IRM-geschützten Nachricht ist.
ms.openlocfilehash: c129370d7920da7cf1f9f32eed2f075e6c21cf8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829803"
---
# <a name="hasirm"></a>HasIrm

Das **HasIrm** -Element gibt an, ob mindestens eine Nachricht in der Unterhaltung und der aktuelle Ordner ein IRM-geschützten Nachricht ist. 
  
```XML
<HasIrm> true | false </HasIrm>
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

Der Textwert der **HasIrm** -Element ist **true** , wenn mindestens eine Nachricht in der Unterhaltung und den aktuellen Ordner IRM hat. Andernfalls ist der Wert **false**.
  
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

