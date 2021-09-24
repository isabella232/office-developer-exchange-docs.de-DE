---
title: ParentItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentItemId
api_type:
- schema
ms.assetid: 72dc4391-72db-44d2-85d9-4718d59886a7
description: Das ParentItemId-Element identifiziert das übergeordnete Element, das mit einer zugeordneten Anlage verknüpft ist.
ms.openlocfilehash: d8072e86d8bd989d4baf6b0f29385dc955b83de8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515362"
---
# <a name="parentitemid"></a>ParentItemId

Das **ParentItemId-Element** identifiziert das übergeordnete Element, das mit einer zugeordneten Anlage verknüpft ist. 
  
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
|**Id** <br/> |Identifiziert ein einzelnes Element im Exchange Speicher, das einer Anlage zugeordnet werden soll. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifies an unspecified version of an item that is identified by the **Id** attribute in the Exchange store. Dies wird verwendet, um sicherzustellen, dass ein aktuelles Element verwendet wird, wenn es mit einer Anlage aktualisiert wird. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Definiert eine Anforderung zum Erstellen einer Anlage zu einem Element in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist im [CreateAttachment-Vorgang](createattachment-operation.md)erforderlich. Dieses Element ist im Wesentlichen identisch mit dem [ItemId-Element.](itemid.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateAttachment-Vorgang](createattachment-operation.md)

