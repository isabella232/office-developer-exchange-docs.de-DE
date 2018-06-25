---
title: ConversationAction
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
description: Das ConversationAction-Element enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757695"
---
# <a name="conversationaction"></a>ConversationAction

Das **ConversationAction** -Element enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
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
|[Aktion (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Enthält die Aktion auf die Unterhaltung vom [ConversationId](conversationid.md) -Element angegeben. Dieses Element muss vorhanden sein.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner der Unterhaltung, die die Aktion durch auf Elemente in der Unterhaltung angewendet [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) -Elements angegeben haben. Dieses Element muss vorhanden sein.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden. Dieses Element muss beim Kopieren, löschen, verschieben und Festlegen von Zustand "gelesen" für Unterhaltungselemente in einem Zielordner vorhanden sein.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Enthält das Datum und die Uhrzeit, zu der der letzten eine Unterhaltung Synchronisierung. Dieses Element muss vorhanden sein, wenn Sie versuchen, um alle Elemente in einer Unterhaltung zu löschen, die bis zu der angegebenen Zeit empfangen wurden.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Gibt an, ob die Antwort gesendet wird, sobald die Aktion startet die Verarbeitung auf dem Server oder gibt an, ob die Antwort gesendet wird, nachdem der Vorgang abgeschlossen wurde. Dieses Element muss vorhanden sein, damit die Antwort für die angeforderte Aktion asynchronen gesendet werden.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Kopie an, und verschieben Sie Aktionen.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, zu denen Elemente in einer Unterhaltung gehören.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Gibt ein Flag, das für alle neuen Elemente in einer Unterhaltung löschen kann.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[DeleteType](deletetype.md) <br/> |Gibt an, wie Elemente in einer Unterhaltung gelöscht werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.  <br/> |
   
## <a name="text-value"></a>Textwert

**Text-Elementwerte ConversationAction**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Kategorisieren Sie der Unterhaltung immer.  <br/> |
|AlwaysDelete  <br/> |Löschen Sie die Unterhaltung immer.  <br/> |
|AlwaysMove  <br/> |Die Unterhaltung verschoben immer.  <br/> |
|Löschen  <br/> |Löschen Sie die Unterhaltung an.  <br/> |
|Verschieben  <br/> |Verschieben der Unterhaltung.  <br/> |
|Kopie  <br/> |Kopieren Sie die Unterhaltung.  <br/> |
|SetReadState  <br/> |Legen Sie den Zustand "gelesen" der Unterhaltung.  <br/> |
|SetRetentionPolicy  <br/> |Legen Sie die Aufbewahrungsrichtlinie für die Unterhaltung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

