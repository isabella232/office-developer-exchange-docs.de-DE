---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: Das DeletedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.
ms.openlocfilehash: f06ca0727916f415c648e876f88bf7eacef5a5ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757911"
---
# <a name="deletedevent"></a>DeletedEvent

Das **DeletedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird. 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

**BaseObjectChangedEventType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Wasserzeichen](watermark.md) <br/> |Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar.  <br/> |
|[Zeitstempel](timestamp.md) <br/> |Den Zeitstempel des ein gelöschtes Postfach-Ereignis Elements oder Ordners darstellt.  <br/> |
|[FolderId](folderid.md) <br/> |Den Bezeichner des gelöschten Ordners darstellt.  <br/> |
|[ItemId](itemid.md) <br/> |Den Bezeichner des gelöschten Elements darstellt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners des gelöschten Elements oder Ordners vor dem Löschen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorgang abonnieren](subscribe-operation.md)  
- [GetEvents-Vorgang](getevents-operation.md)  
- [Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

