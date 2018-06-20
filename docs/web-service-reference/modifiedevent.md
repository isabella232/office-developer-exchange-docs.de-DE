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
description: Das ModifiedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners geändert wird.
ms.openlocfilehash: fb464fb0a270d8ca7d33d40e5425e260970b2f1e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830482"
---
# <a name="modifiedevent"></a>ModifiedEvent

Das **ModifiedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners geändert wird. 
  
```xml
<ModifiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
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
|[Wasserzeichen](watermark.md) <br/> |Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.  <br/> |
|[Zeitstempel](timestamp.md) <br/> |Den Zeitstempel des geänderten Elements oder Ordners Postfach-Ereignisses darstellt.  <br/> |
|[FolderId](folderid.md) <br/> |Den Bezeichner des geänderten Ordners darstellt.  <br/> |
|[ItemId](itemid.md) <br/> |Den Bezeichner des geänderten Elements darstellt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Den Bezeichner des übergeordneten Ordners des geänderten Elements oder Ordners darstellt.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Für jede Änderung eines Elements in einem Ordner werden zwei geänderte Ereignisse generiert. Ein Ereignis ist relevant für das Element, das geändert. Das anderen Ereignis mit ist dem übergeordneten Ordner des Elements relevant. Dies ist die gleichen Ordner wie, dem gegen das Abonnement erstellt wurde. Das Ereignis, das den Ordner zugeordnet ist wird verwendet, um eine mögliche Änderung der [UnreadCount](unreadcount.md) -Eigenschaft auf den Ordner zu kommunizieren. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

