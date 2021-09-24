---
title: NonIndexableItemStatistic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 593e0c79-9ec2-4040-a6a3-3c5c61cbdf7c
description: Das NonIndexableItemStatistic-Element enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnte.
ms.openlocfilehash: 93bdaad2f10adf52ef99f51106596f155af2f18c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509546"
---
# <a name="nonindexableitemstatistic"></a>NonIndexableItemStatistic

Das **NonIndexableItemStatistic-Element** enthält eine einzelne Statistik für ein Element, das nicht indiziert werden konnte. 
  
```XML
<NonIndexableItemStatistic>
   <Mailbox/>
   <ItemCount/>
   <ErrorMessage/>
</NonIndexableItemStatistic>
```

 **NonIndexableItemStatisticType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Postfach (Zeichenfolge)](mailbox-string.md)  |  [ItemCount](itemcount.md)  |  [ErrorMessage](errormessage.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[NonIndexableItemStatistics](nonindexableitemstatistics.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   

