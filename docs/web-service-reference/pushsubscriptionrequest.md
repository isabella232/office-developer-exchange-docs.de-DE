---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: Das PushSubscriptionRequest-Element stellt ein Abonnement für ein Push-basiertes Ereignisbenachrichtigungsabonnement dar.
ms.openlocfilehash: 6eb76bba92e78e048ae97dbec5fc6c4d698a815f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523727"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

Das **PushSubscriptionRequest-Element** stellt ein Abonnement für ein Push-basiertes Ereignisbenachrichtigungsabonnement dar. 
  
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
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von Ordnern verwendet werden, die auf Ereignisbenachrichtigungen überwacht werden sollen.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
|[Watermark](watermark.md) <br/> |Stellt eine Ereignislesemarke in der Postfachereignistabelle dar. Dies wird verwendet, um ein Abonnement zu erstellen, das bei einem Ereignis beginnt, das durch das Wasserzeichen dargestellt wird. Wenn das Wasserzeichen aus einer Subscribe-Anforderung nicht gefunden wird, wird eine Fehlerantwort an den Client zurückgegeben. Dies kann vorkommen, wenn das Wasserzeichen älter als 30 Tage ist oder das Wasserzeichen nie im Postfach vorhanden war.  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |Stellt die in Minuten angegebene Häufigkeit dar, mit der Benachrichtigungen an den Client gesendet werden, wenn keine Ereignisse aufgetreten sind.  <br/> |
|[Url ](url-ex15websvcsotherref.md) <br/> |Stellt den Speicherort des Clientwebdiensts für Pushbenachrichtigungen dar.  <br/> |
   
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



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

