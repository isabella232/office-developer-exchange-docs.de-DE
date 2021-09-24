---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: Das PullSubscriptionRequest-Element stellt ein Abonnement für ein pullbasiertes Ereignisbenachrichtigungsabonnement dar.
ms.openlocfilehash: f1a527dff0c81262cac01a905293af1155acbf1c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540601"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

Das **PullSubscriptionRequest-Element** stellt ein Abonnement für ein pullbasiertes Ereignisbenachrichtigungsabonnement dar. 
  
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
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von Ordnern verwendet werden, die auf Ereignisbenachrichtigungen überwacht werden sollen.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Watermark](watermark.md) <br/> |Stellt eine Ereignislesemarke in der Postfachereignistabelle dar. Dies wird verwendet, um ein Abonnement zu erstellen, das bei einem Ereignis beginnt, das durch das Wasserzeichen dargestellt wird. Wenn das Wasserzeichen aus einer Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben. Dieser Fehler kann auftreten, wenn das Wasserzeichen älter als 30 Tage ist oder das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[Timeout](timeout.md) <br/> |Gibt die Dauer in Minuten an, für die das Abonnement ohne getEvents-Anforderung vom Client im Leerlauf bleiben kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

