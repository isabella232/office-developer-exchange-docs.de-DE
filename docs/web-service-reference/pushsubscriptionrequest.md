---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: Das PushSubscriptionRequest-Element stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.
ms.openlocfilehash: 34717d37b8e5bb50c927e57088299fbcb18a2514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830929"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

Das **PushSubscriptionRequest** -Element stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis. 
  
[Abonnieren](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 **PushSubscriptionRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Gibt an, ob, um alle verfügbaren Ordner zu abonnieren. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren von Ordnern zum Überwachen von ereignisbenachrichtigungen verwendet werden.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Wasserzeichen](watermark.md) <br/> |Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar. Hiermit wird ein Ereignis, dargestellt durch das Wasserzeichen beginnend-Abonnement zu erstellen. Wenn das Wasserzeichen aus die Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben werden soll. Dies kann vorkommen, wenn das Wasserzeichen älter als 30 Tage oder ist wenn das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Stellt die Häufigkeit in Minuten ein, an welche, die Benachrichtigung Nachrichten an den Client gesendet werden, wenn keine Ereignisse eingetreten angegeben.  <br/> |
|[URL](url-ex15websvcsotherref.md) <br/> |Stellt den Speicherort des Webdiensts für Pushbenachrichtigungen-Clients.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

