---
title: Unterhaltung (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: Das Conversation-Element stellt eine einzelne Unterhaltung dar.
ms.openlocfilehash: 7ce75fad17589f4d9a3ca52bcb2041eb1d1f4d2e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515957"
---
# <a name="conversation-conversationtype"></a>Unterhaltung (ConversationType)

Das **Conversation-Element** stellt eine einzelne Unterhaltung dar. 
  
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
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet haben, die derzeit in dieser Unterhaltung in allen Ordnern im Postfach ungelesen sind.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Enthält eine Liste aller Absender von Unterhaltungselementen im Postfach.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Enthält die Übermittlungszeit der Nachricht, die zuletzt in dieser Unterhaltung im aktuellen Ordner empfangen wurde.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Enthält die Übermittlungszeit der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, die auf alle Unterhaltungselemente im aktuellen Ordner angewendet werden.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Enthält den aggregierten Flagstatus für Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Enthält den aggregierten Flagstatus für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement im aktuellen Ordner über eine Anlage verfügt.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens ein Unterhaltungselement in einem Postfach über eine Anlage verfügt.  <br/> |
|[MessageCount](messagecount.md) <br/> |Enthält die Gesamtzahl der Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Enthält die Gesamtanzahl der Unterhaltungselemente im Postfach.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Enthält die Anzahl der ungelesenen Unterhaltungselemente in einem Ordner.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Enthält die Anzahl aller ungelesenen Unterhaltungselemente im Postfach.  <br/> |
|[Größe](size.md) <br/> |Enthält die Unterhaltungsgröße, die aus der Größe aller Unterhaltungselemente im aktuellen Ordner berechnet wird.  <br/> |
|[GlobalSize](globalsize.md) <br/> |Enthält die Größe der Unterhaltung, die aus der Größe aller Unterhaltungselemente im Postfach berechnet wird.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Enthält eine Liste von Elementklassen, die alle Elementklassen der Unterhaltungselemente im aktuellen Ordner darstellt.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Enthält eine Liste der Elementklassen, die alle Elementklassen der Unterhaltungselemente in einem Postfach darstellt.  <br/> |
|[Importance](importance.md) <br/> |Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Enthält die aggregierte Wichtigkeit für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält die Auflistung der Elementbezeichner für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Elementbezeichnern für alle Unterhaltungselemente in einem Postfach.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltungen](conversations-ex15websvcsotherref.md) <br/> |Enthält ein Array von Unterhaltungen, die in der **FindConversation-Antwort** zurückgegeben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

