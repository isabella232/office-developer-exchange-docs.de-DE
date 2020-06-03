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
description: Das PushSubscriptionRequest-Element stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465513"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

Das **PushSubscriptionRequest** -Element stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar. 
  
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
|**SubscribeToAllFolders** <br/> |Gibt an, ob alle verfügbaren Ordner abonniert werden sollen. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu überwachenden Ordnern für Ereignisbenachrichtigungen verwendet werden.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Watermark](watermark.md) <br/> |Stellt eine Ereignis Textmarke in der Tabelle Post Fach Ereignisse dar. Dies wird verwendet, um ein Abonnement zu erstellen, das bei einem durch das Wasserzeichen dargestellten Ereignis beginnt. Wenn das Wasserzeichen aus einer subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben. Dies kann vorkommen, wenn das Wasserzeichen älter als 30 Tage ist oder wenn das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Stellt die in Minuten angegebene Häufigkeit dar, bei der Benachrichtigungsmeldungen an den Client gesendet werden, wenn keine Ereignisse aufgetreten sind.  <br/> |
|[URL](url-ex15websvcsotherref.md) <br/> |Stellt den Speicherort des Client-Webdiensts für Push-Benachrichtigungen dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die zum Erstellen von Abonnements verwendeten Eigenschaften.  <br/> |
   
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



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

