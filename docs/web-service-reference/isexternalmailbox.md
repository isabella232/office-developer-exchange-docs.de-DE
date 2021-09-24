---
title: IsExternalMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: Das IsExternalMailbox -Element gibt an, ob das Postfach befindet sich außerhalb des Unternehmens.
ms.openlocfilehash: f2435356a7315c51f3d99aeedf0ae2b21500981c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524231"
---
# <a name="isexternalmailbox"></a>IsExternalMailbox

Das **IsExternalMailbox** -Element gibt an, ob das Postfach befindet sich außerhalb des Unternehmens. 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchableMailbox](searchablemailbox.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **IsExternalMailbox** -Element gibt an, dass das Postfach in einer externen Organisation ist. Der Wert **false** gibt an, dass das Postfach in der Organisation ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

