---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: Das MakeItemImmutable-Element gibt einen booleschen Wert an, der angibt, ob ein Element schreibgeschützt sein soll.
ms.openlocfilehash: 0e1d28f19492bb6dc013957aa5957b59e791b24b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524826"
---
# <a name="makeitemimmutable"></a>MakeItemImmutable

Das **MakeItemImmutable-Element** gibt einen booleschen Wert an, der angibt, ob ein Element schreibgeschützt sein soll. 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[UpdateItemInRecoverableItems](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a>Textwert

Der Textwert  true für das **MakeItemImmutable-Element** gibt an, dass das Element schreibgeschützt sein soll. Der Wert **"false"** gibt an, dass das Element Lese-/Schreibzugriff zulässt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

