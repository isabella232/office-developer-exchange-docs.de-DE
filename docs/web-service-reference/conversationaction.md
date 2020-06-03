---
title: Unterhaltung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: Das Conversation Action-Element enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529252"
---
# <a name="conversationaction"></a>Unterhaltung

Das **Conversation** Action-Element enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[Unterhaltung](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 **ConversationActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Action (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Enthält die Aktion, die für die durch das [Conversation](conversationid.md) -Element angegebene Konversation ausgeführt werden soll. Dieses Element muss vorhanden sein.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner der Unterhaltung, für die die durch das [Action-Element (ConversationActionTypeType)](action-conversationactiontypetype.md) angegebene Aktion auf Elemente in der Unterhaltung angewendet wird. Dieses Element muss vorhanden sein.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden. Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen des Lese Zustands für Unterhaltungselemente in einem Zielordner vorhanden sein.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Enthält das Datum und die Uhrzeit, zu der eine Unterhaltung zuletzt synchronisiert wurde. Dieses Element muss vorhanden sein, wenn Sie versuchen, alle Elemente in einer Unterhaltung zu löschen, die bis zur angegebenen Zeit empfangen wurden.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Gibt an, ob die Antwort gesendet wird, sobald die Aktion auf dem Server verarbeitet wird oder ob die Antwort gesendet wird, nachdem die Aktion abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort asynchron an die angeforderte Aktion gesendet werden kann.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Aktionen kopieren und verlegen an.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, zu denen Elemente in einer Unterhaltung gehören.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Gibt ein Flag an, das das Löschen für alle neuen Elemente in einer Unterhaltung ermöglicht.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[Deletetypeharddelete](deletetype.md) <br/> |Gibt an, wie Elemente in einer Unterhaltung gelöscht werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Enthält eine Auflistung von Unterhaltungen und die Aktionen, die auf diese angewendet werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

**Textwerte des Conversation-Elementtexts**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Unterhaltung immer kategorisieren.  <br/> |
|Alwaysdeleteolalwaysdelete  <br/> |Die Unterhaltung wird immer gelöscht.  <br/> |
|AlwaysMove  <br/> |Die Unterhaltung immer verlagern.  <br/> |
|Löschen  <br/> |Löschen Sie die Unterhaltung.  <br/> |
|Move  <br/> |Die Unterhaltung zu verlegen.  <br/> |
|Copy  <br/> |Kopieren Sie die Unterhaltung.  <br/> |
|SetReadState  <br/> |Legen Sie den Lesestatus der Unterhaltung fest.  <br/> |
|SetRetentionPolicy  <br/> |Legen Sie die Aufbewahrungsrichtlinie für die Unterhaltung fest.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

