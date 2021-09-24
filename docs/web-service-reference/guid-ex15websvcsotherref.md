---
title: Guid
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 49dcf69f-bf8d-4be6-a24c-03bbd13f4fe5
description: Das Guid-Element gibt den global eindeutigen Bezeichner des Postfachs an.
ms.openlocfilehash: 093364e26d5c65127c1f23214e1d3d0aa85c95c2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519534"
---
# <a name="guid"></a>Guid

Das **Guid-Element** gibt den global eindeutigen Bezeichner des Postfachs an. 
  
```XML
<Guid></Guid>
```

 **GuidType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchableMailbox](searchablemailbox.md) <br/> |Gibt ein Postfach an, das von einer **GetSearchableMailboxes-Anforderung** zurückgegeben wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Guid-Elements** ist ein GUID-Wert, der ein Postfach eindeutig identifiziert. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

