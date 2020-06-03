---
title: MovedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MovedEvent
api_type:
- schema
ms.assetid: 572f8b40-dfa8-47bc-b0c1-e1a7138506fd
description: Das MovedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.
ms.openlocfilehash: 1f8fb57dba7edb769fe0dd658d89c032dccf8c5f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530408"
---
# <a name="movedevent"></a>MovedEvent

Das **MovedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird. 
  
```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldItemId/>
   <OldParentFolderId/>
</MovedEvent>
```

```xml
<MovedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</MovedEvent>
```


**MovedCopiedEventType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Stellt ein Lesezeichen für Ereignisse in der Tabelle Post Fach Ereignisse dar.  <br/> |
|[Timestamp](timestamp.md) <br/> |Stellt den Zeitstempel des Post Fach Ereignisses "Element/Ordner Verschiebe" dar.  <br/> |
|[FolderId](folderid.md) <br/> |Stellt den Bezeichner des verschobenen Ordners dar.  <br/> |
|[ItemId](itemid.md) <br/> |Stellt den Bezeichner des verschobenen Elements dar.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des Ordners dar, der das verschobene Element oder den verschobenen Ordner enthält.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Enthält den Ordner Bezeichner des ursprünglichen Ordners, bevor er verschoben oder kopiert wurde.  <br/> |
|[OldItemId](olditemid.md) <br/> |Enthält die eindeutige ID des ursprünglichen Elements, bevor es verschoben wurde.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Enthält den Bezeichner des ursprünglichen übergeordneten Ordners eines verschobenen Elements oder Ordners.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

