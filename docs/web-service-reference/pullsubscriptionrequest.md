---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: Das PullSubscriptionRequest-Element stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.
ms.openlocfilehash: fb9712c9e1481678c2821ee344052783d5c25bf9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468866"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

Das **PullSubscriptionRequest** -Element stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar. 
  
[Abonnieren](subscribe.md)
  
[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 **PullSubscriptionRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Gibt an, ob alle verfügbaren Ordner abonniert werden sollen. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu überwachenden Ordnern für Ereignisbenachrichtigungen verwendet werden.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Watermark](watermark.md) <br/> |Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar. Dies wird verwendet, um ein Abonnement zu erstellen, das bei einem Ereignis beginnt, das durch das Wasserzeichen dargestellt wird. Wenn das Wasserzeichen aus einer subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben. Dieser Fehler kann auftreten, wenn das Wasserzeichen älter als 30 Tage ist oder wenn das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[Timeout](timeout.md) <br/> |Stellt die Dauer in Minuten dar, in der das Abonnement ohne eine GetEvents-Anforderung vom Client im Leerlauf bleiben kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

