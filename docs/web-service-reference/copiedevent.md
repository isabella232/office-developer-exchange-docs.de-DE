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
description: Das CopiedEvent-Element stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.
ms.openlocfilehash: 89ca9fb1fd2f4187efdec0e087d840bfee197a29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757716"
---
# <a name="copiedevent"></a>CopiedEvent

Das **CopiedEvent** -Element stellt ein Ereignis in der eines Elements oder Ordners kopiert wird. 
  
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

 **MovedCopiedEventType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Wasserzeichen](watermark.md) <br/> |Stellt eine Textmarke Ereignisse in der Tabelle der Postfach-Ereignisse dar.  <br/> |
|[Zeitstempel](timestamp.md) <br/> |Steht für den Zeitstempel eines Ereignisses Postfach Element-Ordner kopieren.  <br/> |
|[FolderId](folderid.md) <br/> |Den Bezeichner des Ordners darstellt.  <br/> |
|[ItemId](itemid.md) <br/> |Den Bezeichner des Elements darstellt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des Ordners, der die Kopie enthält.  <br/> |
|[OldFolderId](oldfolderid.md) <br/> |Die Ordner-ID des ursprünglichen Ordners darstellt, bevor sie kopiert wurde.  <br/> |
|[OldItemId](olditemid.md) <br/> |Enthält die eindeutige ID des ursprünglichen Elements an, bevor sie kopiert wurde.  <br/> |
|[OldParentFolderId](oldparentfolderid.md) <br/> |Enthält den Bezeichner des übergeordneten Ordners ursprünglichen eines Elements oder Ordners, der kopiert wurde.  <br/> |
   
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



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


[Mithilfe von Pullabonnements](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[Beispielanwendung für Pushbenachrichtigungen](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

