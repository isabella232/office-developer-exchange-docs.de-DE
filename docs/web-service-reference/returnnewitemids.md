---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: Das ReturnNewItemIds-Element gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.
ms.openlocfilehash: 003676c4c034454aa551e42bf3af976183117b8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465114"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

Das **ReturnNewItemIds** -Element gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden. 
  
```XML
<ReturnNewItemIds/>
```

 **xs: Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange-Informationsspeicher.  <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **ReturnNewItemIds** -Element gibt an, dass die neuen Elementbezeichner in der Antwort zurückgegeben werden. Der Wert **false** gibt an, dass die neuen Elementbezeichner nicht in der Antwort zurückgegeben werden. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

