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
description: Das MovedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.
ms.openlocfilehash: 07f9c02ea194187a9fdfb1e27b19eb311392f51f
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353259"
---
# <a name="movedevent"></a>MovedEvent

Das **MovedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird. 
  
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
|[Watermark](watermark.md) <br/> |Stellt eine Textmarke Ereignisse in der Tabelle der Postfach-Ereignisse dar.  <br/> |
|[TimeStamp](timestamp.md) <br/> |Stellt den Zeitstempel der ein Element-Ordner Postfach-Ereignis.  <br/> |
|[FolderId](folderid.md) <br/> |Den Bezeichner des verschobenen Ordners darstellt.  <br/> |
|[ItemId](itemid.md) <br/> |Stellt die das verschobene Element-ID an.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des Ordners, die das verschobene Element oder Ordner enthält.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Die Ordner-ID des ursprünglichen Ordners enthält, bevor sie verschoben oder kopiert wurde.  <br/> |
|[OldItemId](olditemid.md) <br/> |Enthält die eindeutige ID des ursprünglichen Elements an, bevor sie verschoben wurde.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Enthält den Bezeichner des übergeordneten Ordners ursprünglichen eines Elements oder Ordners, die verschoben wurde.  <br/> |
   
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

