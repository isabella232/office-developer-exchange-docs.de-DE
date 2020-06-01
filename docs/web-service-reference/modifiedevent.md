---
title: ModifiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ModifiedEvent
api_type:
- schema
ms.assetid: ca1309f4-2df7-4289-811c-75c3db0e7072
description: Das ModifiedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.
ms.openlocfilehash: 1a798773601a0857b9064c7fa6a532a7a36517ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468551"
---
# <a name="modifiedevent"></a>ModifiedEvent

Das **ModifiedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird. 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/> 
   <ParentFolderId/>
   <UnreadCount/>
</ModifiedEvent>
```

**ModifiedEventType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar.  <br/> |
|[Timestamp](timestamp.md) <br/> |Stellt den Zeitstempel eines geänderten Element-oder Ordner Postfach-Ereignisses dar.  <br/> |
|[FolderId](folderid.md) <br/> |Stellt den Bezeichner des geänderten Ordners dar.  <br/> |
|[ItemId](itemid.md) <br/> |Stellt den Bezeichner des geänderten Elements dar.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners des geänderten Elements oder Ordners dar.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Stellt die Anzahl der ungelesenen Elemente in einem bestimmten Ordner dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für jede Änderung eines Elements in einem Ordner werden zwei geänderte Ereignisse generiert. Ein Ereignis ist für das geänderte Element relevant. Das andere Ereignis ist für den übergeordneten Ordner des Elements relevant. Dies ist derselbe Ordner, für den das Abonnement erstellt wurde. Das Ereignis, das dem Ordner zugeordnet ist, wird verwendet, um eine mögliche Änderung an der [UnreadCount](unreadcount.md) -Eigenschaft für den Ordner zu kommunizieren. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorgang abonnieren](subscribe-operation.md)  
- [GetEvents-Vorgang](getevents-operation.md)  
- [Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

