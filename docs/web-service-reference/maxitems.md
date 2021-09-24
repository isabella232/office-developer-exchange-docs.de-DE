---
title: MaxItems
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: Das MaxItems-Element gibt die maximale Anzahl von Elementen an, die in der Anforderung zurückgegeben werden sollen.
ms.openlocfilehash: 23a78db874ef3678be8c6703fb7004fc5f8a1425
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511116"
---
# <a name="maxitems"></a>MaxItems

Das **MaxItems-Element** gibt die maximale Anzahl von Elementen an, die in der Anforderung zurückgegeben werden sollen. 
  
```XML
<MaxItems/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetReminders](getreminders.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **MaxItems-Elements** ist die maximale Anzahl von Elementen, die in der Anforderung zurückgegeben werden sollen. Diese Zahl darf nicht kleiner als Null oder größer als 200 sein. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetReminders](getreminders.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

