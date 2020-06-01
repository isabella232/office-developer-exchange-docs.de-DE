---
title: MaximumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fb7c3ab3-ef97-44c7-83e0-93cfe8c48e84
description: Das MaximumSize-Element stellt die maximale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: 250e0c6aed37b934f5cf6eaed9d93b9f56159d93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461751"
---
# <a name="maximumsize"></a>MaximumSize

Das **MaximumSize** -Element stellt die maximale Größe dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<Maximum/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die Mindest-und Höchstgröße an, die eingehende Nachrichten aufweisen müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die die maximale Größe der Nachricht in Bytes angibt.
  
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



[Minimum Size](minimumsize.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

