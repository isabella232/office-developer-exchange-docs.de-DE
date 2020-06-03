---
title: IsReadReceipt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReadReceipt
api_type:
- schema
ms.assetid: e60e525f-c136-469a-b68b-b3dc01f400a6
description: Das IsReadReceipt-Element gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: e86a7776bc43204dae9fc92f21d4304255ddb888
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463902"
---
# <a name="isreadreceipt"></a>IsReadReceipt

Das **IsReadReceipt** -Element gibt an, ob eingehende Nachrichten Lesebestätigungen sein müssen, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<IsReadReceipt> true | false</IsReadReceipt>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen, die beim erfüllt, wird die Regelaktionen für diese Regel ausgelöst.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** gibt an, dass die Nachricht eine Lesebestätigung sein muss, damit die Bedingung oder Ausnahme zutrifft. Wenn die Nachricht nicht eine Lesebestätigung sein muss, damit die Bedingung oder Ausnahme angewendet wird, ist der Wert **false**.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

