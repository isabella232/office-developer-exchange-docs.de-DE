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
description: Das Unterhaltung-Element darstellt, einem einzelnen Gespräch.
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757696"
---
# <a name="conversation-conversationtype"></a>Unterhaltung (ConversationType)

Das **Unterhaltung** -Element darstellt, einem einzelnen Gespräch. 
  
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
|[ConversationId](conversationid.md) <br/> |Stellt die ID einer Unterhaltung.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Stellt das gleichen Thema. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueRecipients](uniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung aus einem bestimmten Ordner aggregiert. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueRecipients](globaluniquerecipients.md) <br/> |Enthält die Empfängerliste einer Unterhaltung über ein Postfach aggregiert. Dieses Element ist schreibgeschützt.  <br/> |
|[UniqueUnreadSenders](uniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung im aktuellen Ordner ungelesen sind. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueUnreadSenders](globaluniqueunreadsenders.md) <br/> |Enthält eine Liste aller Personen, die Nachrichten gesendet wurden, die derzeit in dieser Unterhaltung ungelesen in allen Ordnern im Postfach sind.  <br/> |
|[UniqueSenders](uniquesenders.md) <br/> |Enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[GlobalUniqueSenders](globaluniquesenders.md) <br/> |Enthält eine Liste von allen Absendern von Unterhaltungselementen im Postfach.  <br/> |
|[LastDeliveryTime](lastdeliverytime.md) <br/> |Enthält die Uhrzeit der Übermittlung der Nachricht, die in dieser Unterhaltung im aktuellen Ordner zuletzt empfangen wurde.  <br/> |
|[GlobalLastDeliveryTime](globallastdeliverytime.md) <br/> |Enthält die Uhrzeit der Übermittlung der Nachricht, die zuletzt in dieser Unterhaltung in allen Ordnern im Postfach empfangen wurde.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, die auf alle Unterhaltungselemente im aktuellen Ordner angewendet werden.  <br/> |
|[GlobalCategories](globalcategories.md) <br/> |Enthält die Kategorieliste für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[FlagStatus](flagstatus.md) <br/> |Enthält den aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.  <br/> |
|[GlobalFlagStatus](globalflagstatus.md) <br/> |Enthält den aggregierten Kennzeichnungsstatus für alle Unterhaltungselemente in einem Postfach an.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement im aktuellen Ordner eine Anlage enthält.  <br/> |
|[GlobalHasAttachments](globalhasattachments.md) <br/> |Enthält einen Wert, der angibt, ob mindestens eine unterhaltungselement in einem Postfach eine Anlage enthält.  <br/> |
|[MessageCount](messagecount.md) <br/> |Enthält die Gesamtanzahl der Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalMessageCount](globalmessagecount.md) <br/> |Die Gesamtzahl der Unterhaltungselemente im Postfach enthält.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Enthält die Anzahl der ungelesenen Unterhaltungselemente innerhalb eines Ordners.  <br/> |
|[GlobalUnreadCount](globalunreadcount.md) <br/> |Anzahl der ungelesenen Unterhaltungselemente im Postfach enthält.  <br/> |
|[Size](size.md) <br/> |Enthält die Unterhaltung Größe von der Größe aller Unterhaltung Elemente im aktuellen Ordner berechnet.  <br/> |
|[GlobalSize ist](globalsize.md) <br/> |Enthält die Größe der Unterhaltung von der Größe aller Unterhaltung Elemente im Postfach berechnet.  <br/> |
|[ItemClasses (ArrayOfItemClassType)](itemclasses-arrayofitemclasstype.md) <br/> |Enthält eine Liste der Element-Klassen, die die Element-Klassen der Unterhaltungselemente im aktuellen Ordner darstellt.  <br/> |
|[GlobalItemClasses](globalitemclasses.md) <br/> |Enthält eine Liste der Element-Klassen, die die Element-Klassen der Unterhaltungselemente in einem Postfach darstellt.  <br/> |
|[Importance](importance.md) <br/> |Enthält die aggregierte Bedeutung für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalImportance](globalimportance.md) <br/> |Enthält die aggregierte Bedeutung für alle Unterhaltungselemente in einem Postfach an.  <br/> |
|[Artikelnummern ein.](itemids.md) <br/> |Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente im aktuellen Ordner.  <br/> |
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Conversations](conversations-ex15websvcsotherref.md) <br/> |Enthält ein Array von Unterhaltungen, die in der Antwort **FindConversation** zurückgegeben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


[Conversations in EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

