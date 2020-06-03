---
title: ItemHoldPeriod
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 30369db5-4d45-40e8-bc83-3236667fc404
description: Das ItemHoldPeriod-Element gibt den Zeitraum an, in dem Inhalte aufbewahrt werden sollen, die mit der Post Fach Abfrage übereinstimmen.
ms.openlocfilehash: 185666b72cc96dd88605b7baa6433d070e7ebc91
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452286"
---
# <a name="itemholdperiod"></a>ItemHoldPeriod

Das **ItemHoldPeriod** -Element gibt den Zeitraum an, in dem Inhalte aufbewahrt werden sollen, die mit der Post Fach Abfrage übereinstimmen. 
  
```XML
<ItemHoldPeriod/>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SetHoldOnMailboxes](setholdonmailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert kann "unbegrenzt" oder der Zeichenfolgenwert eines beliebigen [TimeSpan](https://msdn.microsoft.com/library/1ecy8h51%28v=vs.110%29.aspx) -Werts sein. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SetHoldOnMailboxes](setholdonmailboxes.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

