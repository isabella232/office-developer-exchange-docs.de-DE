---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: Das ReturnNewItemIds-Element gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.
ms.openlocfilehash: 93ff4e37c56c3583e81711ba7e3582706d9ef940
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512380"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

Das **ReturnNewItemIds-Element** gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden. 
  
```XML
<ReturnNewItemIds/>
```

 **xs:boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange Speicher.  <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung zum Verschieben eines Elements im Exchange Speicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert  true für das **ReturnNewItemIds-Element** gibt an, dass die neuen Elementbezeichner in der Antwort zurückgegeben werden. Der Wert **"false"** gibt an, dass die neuen Elementbezeichner in der Antwort nicht zurückgegeben werden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

