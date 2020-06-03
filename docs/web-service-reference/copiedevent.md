---
title: CopiedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopiedEvent
api_type:
- schema
ms.assetid: 82f2fcac-deaa-4ff8-801f-4fe28d8a19f5
description: Das CopiedEvent-Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.
ms.openlocfilehash: 928910ddbe0bf1e48549d1665ab373f7382366d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529245"
---
# <a name="copiedevent"></a>CopiedEvent

Das **CopiedEvent** -Element stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird. 
  
```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <FolderId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
```

```xml
<CopiedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
   <OldFolderId/>
   <OldParentFolderId/>
</CopiedEvent>
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
|[Timestamp](timestamp.md) <br/> |Stellt den Zeitstempel eines Post Fach Ereignisses zum Kopieren von Elementen/Ordnern dar.  <br/> |
|[FolderId](folderid.md) <br/> |Stellt den Bezeichner des Ordners dar.  <br/> |
|[ItemId](itemid.md) <br/> |Stellt den Bezeichner des Elements dar.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des Ordners dar, der die Kopie enthält.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Stellt die Ordner-ID des ursprünglichen Ordners vor dem Kopieren dar.  <br/> |
|[OldItemId](olditemid.md) <br/> |Enthält den eindeutigen Bezeichner des ursprünglichen Elements, bevor es kopiert wurde.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Enthält den Bezeichner des ursprünglichen übergeordneten Ordners eines Elements oder Ordners, das kopiert wurde.  <br/> |
   
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
- [Verwenden von Pullabonnements](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx) 
- [Beispielanwendung für Pushbenachrichtigungen](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

