---
title: Ignorieren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Ignore
api_type:
- schema
ms.assetid: 7789eec5-ceec-43f2-84d5-d0d15b734076
description: Das Ignore-Element identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen.
ms.openlocfilehash: 92501b2166647c80f8515a27f443b23af14c08dc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514606"
---
# <a name="ignore"></a>Ignorieren

Das **Ignore-Element** identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen. 
  
[SyncFolderItems](syncfolderitems.md)
  
[Ignore](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 **ArrayOfBaseItemIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

