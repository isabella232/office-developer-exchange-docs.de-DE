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
description: Das PullSubscriptionRequest-Element stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.
ms.openlocfilehash: 5f757bf1f79f7e2a00fb886db50e6ea0eaed1a4a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830932"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

Das **PullSubscriptionRequest** -Element stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis. 
  
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
|**SubscribeToAllFolders** <br/> |Gibt an, ob, um alle verfügbaren Ordner zu abonnieren. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren von Ordnern zum Überwachen von ereignisbenachrichtigungen verwendet werden.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Wasserzeichen](watermark.md) <br/> |Stellt eine Textmarke Ereignis in der Tabelle der Postfach-Ereignisse dar. Hiermit wird ein Abonnement, die beginnt am ein Ereignis zu erstellen, die durch das Wasserzeichen dargestellt wird. Wenn das Wasserzeichen aus die Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben werden soll. Dieser Fehler kann auftreten, wenn das Wasserzeichen älter als 30 Tage oder ist wenn das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[Timeout](timeout.md) <br/> |Stellt die Dauer in Minuten, die das Abonnement ohne GetEvents Anforderung vom Client im Leerlauf sein kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.  <br/> |
   
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



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

