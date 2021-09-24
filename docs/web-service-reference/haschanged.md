---
title: HasChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 15ff513d-f39e-44ed-a13f-ab3f86fa37e1
description: Das HasChanged-Element gibt an, ob sich das Foto eines Benutzers geändert hat.
ms.openlocfilehash: 456660272815aac27ea99919eb92a02f754fb4ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516790"
---
# <a name="haschanged"></a>HasChanged

Das **HasChanged-Element** gibt an, ob sich das Foto eines Benutzers geändert hat. 
  
```XML
<HasChanged> true | false </HasChanged>
```

 ****
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetUserPhotoResponse](getuserphotoresponse.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **HasChanged-Element** gibt an, dass sich das Foto seit der letzten Rückgabe geändert hat. Der Wert **"false"** gibt an, dass sich das Foto seit der letzten Rückgabe nicht geändert hat. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

