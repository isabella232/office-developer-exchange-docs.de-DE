---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: Das StreamingSubscriptionRequest-Element stellt ein Abonnement für ein Streaming-Ereignis Benachrichtigungsabonnement dar.
ms.openlocfilehash: b469ba7598420189c1db0e2fe676a279390eb6bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468229"
---
# <a name="streamingsubscriptionrequest"></a>StreamingSubscriptionRequest

Das **StreamingSubscriptionRequest** -Element stellt ein Abonnement für ein Streaming-Ereignis Benachrichtigungsabonnement dar. 
  
[Abonnieren](subscribe.md)
  
[StreamingSubscriptionRequest](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 **StreamingSubscriptionRequest**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |Gibt an, ob der Server für alle Ordner im Postfach des Benutzers abonniert werden soll. Der Wert **true** gibt an, dass der Server abonniert wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu überwachenden Ordnern für Ereignisbenachrichtigungen verwendet werden.  <br/> |
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignisbenachrichtigungen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnieren](subscribe.md) <br/> |Enthält die Eigenschaften, die zum Erstellen von Abonnements verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
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
  
[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

