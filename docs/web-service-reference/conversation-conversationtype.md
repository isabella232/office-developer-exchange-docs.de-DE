---
title: Unterhaltung (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: Das Conversation-Element stellt eine einzelne Unterhaltung dar.
ms.openlocfilehash: 9969a6cfe1f977b1c24e03771f231f4eb03d1ac6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458936"
---
# <a name="conversation-conversationtype"></a>Unterhaltung (ConversationType)

Das **Conversation** -Element stellt eine einzelne Unterhaltung dar. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 **ConversationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationId](conversationid.md) <br/> |Stellt den Bezeichner einer Unterhaltung dar.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Stellt das Unterhaltungsthema dar. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung, die aus einem bestimmten Ordner aggregiert wurde. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung, die über ein Postfach aggregiert wurde. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in dem aktuellen Ordner nicht gelesen wurden. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung für alle Ordner im Postfach ungelesen sind.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Enthält die Zustellungszeit der Nachricht, die zuletzt in dieser Unterhaltung über alle Ordner im Postfach empfangen wurde.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, die auf alle Unterhaltungselemente im aktuellen Ordner angewendet werden.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Enthält die Kategorienliste für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Enthält den aggregierten Kennzeichen Status für Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Enthält den aggregierten Kennzeichen Status für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement im aktuellen Ordner eine Anlage aufweist.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement in einem Postfach eine Anlage aufweist.  <br/> |
|[MessageCount](messagecount.md) <br/> |Enthält die Gesamtzahl der Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Enthält die Gesamtzahl der Unterhaltungselemente im Postfach.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Enthält die Anzahl der ungelesenen Unterhaltungselemente in einem Ordner.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Enthält die Anzahl aller ungelesenen Unterhaltungselemente im Postfach.  <br/> |
|[Größe](size.md) <br/> |Enthält die von der Größe aller Unterhaltungselemente im aktuellen Ordner berechnete Unterhaltungs Größe.  <br/> |
|[Globals](globalsize.md) <br/> |Enthält die Größe der Unterhaltung, die von der Größe aller Unterhaltungselemente im Postfach berechnet wird.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente im aktuellen Ordner darstellt.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente in einem Postfach darstellt.  <br/> |
|[Importance](importance.md) <br/> |Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltungen](conversations-ex15websvcsotherref.md) <br/> |Enthält ein Array von Unterhaltungen, die in der **FindConversation** -Antwort zurückgegeben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

