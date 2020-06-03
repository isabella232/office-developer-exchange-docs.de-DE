---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: Das GetItem-Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: a02403ee84195a41387d5dbe1785ae6d12b47da5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458698"
---
# <a name="getitem"></a>GetItem

Das **GetItem** -Element definiert eine Anforderung zum Abrufen eines Elements aus einem Postfach im Exchange-Informationsspeicher. 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 **GetItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und Inhalte, die in einer **GetItem** -Antwort enthalten sein sollen.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält die eindeutigen Identitäten von Elementen, vorkommen-Elementen und wiederkehrenden Gestaltungsvorlagen, die zum Abrufen von Elementen aus dem Exchange-Informationsspeicher verwendet werden. Diese Elemente stellen Kontakte, Aufgaben, Nachrichten, Kalenderelemente, Besprechungsanfragen und andere gültige Elemente in einem Postfach dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetItem-Vorgang](getitem-operation.md)

