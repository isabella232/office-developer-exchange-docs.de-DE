---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: Das SuppressReadReceipts-Element gibt an, ob Lesebestätigungen unterdrückt werden sollen.
ms.openlocfilehash: 1f63f46f4e74a3123661caba39b737910bc2ef30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517651"
---
# <a name="suppressreadreceipts"></a>SuppressReadReceipts

Das **SuppressReadReceipts-Element** gibt an, ob Lesebestätigungen unterdrückt werden sollen. 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[ConversationAction](conversationaction.md)  |  [MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **SuppressReadReciepts-Element** gibt an, dass Lesebestätigungen unterdrückt werden. Der Wert **"false"** gibt an, dass Lesebestätigungen an den Absender gesendet werden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

