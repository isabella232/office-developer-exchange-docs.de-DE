---
title: IncludeNonIndexableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: af7f202b-2889-447e-bdeb-aaad18ce6b46
description: Das IncludeNonIndexableItems-Element enthält einen booleschen Wert, um anzugeben, ob Elemente eingeschlossen werden sollen, die nicht indiziert werden können.
ms.openlocfilehash: 33ff8c59c3ef1d9a91f87870e0a876c5a39ce795
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514599"
---
# <a name="includenonindexableitems"></a>IncludeNonIndexableItems

Das **IncludeNonIndexableItems-Element** enthält einen **booleschen** Wert, um anzugeben, ob Elemente eingeschlossen werden sollen, die nicht indiziert werden können. 
  
```XML
<IncludeNonIndexableItems>true | false</IncludeNonIndexableItems>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IncludeNonIndexableItems-Element** gibt an, dass Elemente, die nicht indiziert werden können, in Postfacharchiven enthalten sind. Der Wert **"false"** gibt an, dass die Elemente, die nicht indiziert werden können, nicht in postfacharchiven enthalten sind. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

