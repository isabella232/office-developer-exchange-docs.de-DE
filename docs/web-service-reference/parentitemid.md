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
description: Das ParentItemId-Element identifiziert das übergeordnete Element, das auf eine zugeordnete Anlage verweist.
ms.openlocfilehash: 4f3e33da0af2438948313f0e335cd03e076d135a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465744"
---
# <a name="parentitemid"></a>ParentItemId

Das **ParentItemId** -Element identifiziert das übergeordnete Element, das auf eine zugeordnete Anlage verweist. 
  
- [CreateAttachment](createattachment.md)
  
- [ParentItemId](parentitemid.md)
  
```xml
<ParentItemId Id="" ChangeKey="" />
```

**Itemidtype**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Bezeichnet ein einzelnes Element im Exchange-Informationsspeicher, das einer Anlage zugeordnet werden soll. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Gibt eine nicht angegebene Version eines Elements an, das durch das **ID-** Attribut im Exchange-Informationsspeicher identifiziert wird. Dies wird verwendet, um sicherzustellen, dass ein aktuelles Element verwendet wird, wenn es mit einer Anlage aktualisiert wird. Dieser Wert ist eine Zeichenfolge. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Definiert eine Anforderung zum Erstellen einer Anlage für ein Element in einem Postfach.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CreateAttachment` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist im [CreateAttachment-Vorgang](createattachment-operation.md)erforderlich. Dieses Element ist im Wesentlichen identisch mit dem [ItemID](itemid.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |[https://schemas.microsoft.com/exchange/services/2006/messages](https://schemas.microsoft.com/exchange/services/2006/messages) <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateAttachment-Vorgang](createattachment-operation.md)

