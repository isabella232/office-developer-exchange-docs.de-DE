---
title: IsPermanentFailure
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 18dc3a97-cc0a-4092-934e-a6e86f52e668
description: Das IsPermanentFailure-Element gibt an, ob ein vorheriger Versuch, das Element zu indizieren, nicht erfolgreich war.
ms.openlocfilehash: e5ed20de3c3de9c39d1487e3177c1b6ec358d990
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532720"
---
# <a name="ispermanentfailure"></a>IsPermanentFailure

Das **IsPermanentFailure-Element** gibt an, ob ein vorheriger Versuch, das Element zu indizieren, nicht erfolgreich war. 
  
```XML
<IsPermanentFailure>true | false</IsPermanentFailure>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[NonIndexableItemDetail](nonindexableitemdetail.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IsPermanentFailure-Element** gibt an, dass ein vorheriger Versuch, das Postfachelement zu indizieren, nicht erfolgreich war. Der Wert **"false"** gibt an, dass ein vorheriger Versuch zum Indizierung des Postfachelements erfolgreich war. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

