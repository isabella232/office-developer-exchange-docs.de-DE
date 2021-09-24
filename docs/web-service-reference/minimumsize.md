---
title: MinimumSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 841d229c-140c-48bd-b3a7-21478fcea2fb
description: Das MinimumSize-Element stellt die Mindestgröße dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft.
ms.openlocfilehash: c3f1284a5a82731093863b0a621bcf2f7f55cf22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540650"
---
# <a name="minimumsize"></a>MinimumSize

Das **MinimumSize-Element** stellt die Mindestgröße dar, die eine Nachricht aufweisen muss, damit die Bedingung oder Ausnahme zutrifft. 
  
```XML
<MinimumSize/>
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
|[WithinSizeRange](withinsizerange.md) <br/> |Gibt die minimale und maximale Größe an, die eingehende Nachrichten haben müssen, damit die Bedingung oder Ausnahme zutrifft.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist eine ganze Zahl, die die Mindestgröße der Nachricht in Byte angibt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MaximumSize](maximumsize.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

