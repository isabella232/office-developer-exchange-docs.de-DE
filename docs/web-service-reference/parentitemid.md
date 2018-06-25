---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: Das ParentItemId-Element identifiziert das übergeordnete Element, das mit Anlage zugeordneten verknüpft.
ms.openlocfilehash: 9bd875ee5ead8b87996288a640e1bb14e3a5e8b8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830703"
---
# <a name="parentitemid"></a>ParentItemId

Das **ParentItemId** -Element identifiziert das übergeordnete Element, das mit Anlage zugeordneten verknüpft. 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**ItemIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Gibt ein einzelnes Element in der Exchange-Informationsspeicher, die eine Anlage zugeordnet. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifiziert eine nicht spezifizierte Version eines Elements, das durch das **Id** -Attribut im Exchange-Speicher identifiziert wird. Dies wird verwendet, um sicherzustellen, dass ein aktuelles Element verwendet wird, wenn es mit einer Anlage aktualisiert wird. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Definiert eine Anforderung an eine Anlage zu einem Element in einem Postfach zu erstellen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wird in den [CreateAttachment Vorgang](createattachment-operation.md)erforderlich. Dieses Element ist im Wesentlichen identisch mit dem [ItemId](itemid.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |[http://schemas.microsoft.com/exchange/services/2006/messages](http://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateAttachment-Vorgang](createattachment-operation.md)

