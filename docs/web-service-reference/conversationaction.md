---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: Das ConversationAction-Element enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.
ms.openlocfilehash: 04af68b4ad8442160792fd3aa9f3259058a0f3a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531106"
---
# <a name="conversationaction"></a>ConversationAction

Das **ConversationAction-Element** enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll. 
  
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
|[Aktion (ConversationActionTypeType)](action-conversationactiontypetype.md) <br/> |Enthält die Aktion, die für die vom [ConversationId-Element](conversationid.md) angegebene Unterhaltung ausgeführt werden soll. Dieses Element muss vorhanden sein.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner der Unterhaltung, auf die die durch das [Action-Element (ConversationActionTypeType)-Element](action-conversationactiontypetype.md) angegebene Aktion auf Elemente in der Unterhaltung angewendet wird. Dieses Element muss vorhanden sein.  <br/> |
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Aktionen bestimmt ist, die Ordner verwenden. Dieses Element muss beim Kopieren, Löschen, Verschieben und Festlegen des Lesestatus von Unterhaltungselementen in einem Zielordner vorhanden sein.  <br/> |
|[ConversationLastSyncTime](conversationlastsynctime.md) <br/> |Enthält das Datum und die Uhrzeit der letzten Synchronisierung einer Unterhaltung. Dieses Element muss vorhanden sein, wenn versucht wird, alle Elemente in einer Unterhaltung zu löschen, die bis zum angegebenen Zeitpunkt empfangen wurden.  <br/> |
|[ProcessRightAway](processrightaway.md) <br/> |Gibt an, ob die Antwort gesendet wird, sobald die Aktion mit der Verarbeitung auf dem Server beginnt, oder ob die Antwort nach Abschluss der Aktion gesendet wird. Dieses Element muss vorhanden sein, damit die Antwort asynchron zu der angeforderten Aktion gesendet wird.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für Kopier- und Verschiebungsaktionen an.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Enthält eine Auflistung von Zeichenfolgen, die die Kategorien identifizieren, zu denen Elemente in einer Unterhaltung gehören.  <br/> |
|[EnableAlwaysDelete](enablealwaysdelete.md) <br/> |Gibt ein Kennzeichen an, das das Löschen aller neuen Elemente in einer Unterhaltung ermöglicht.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[DeleteType](deletetype.md) <br/> |Gibt an, wie Elemente in einer Unterhaltung gelöscht werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationActions](conversationactions.md) <br/> |Enthält eine Auflistung von Unterhaltungen und die Aktionen, die auf sie angewendet werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

**Textwerte des ConversationAction-Elements**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|AlwaysCategorize  <br/> |Kategorisieren Sie die Unterhaltung immer.  <br/> |
|AlwaysDelete  <br/> |Löschen Sie immer die Unterhaltung.  <br/> |
|AlwaysMove  <br/> |Verschieben Sie die Unterhaltung immer.  <br/> |
|Löschen  <br/> |Löschen Sie die Unterhaltung.  <br/> |
|Move  <br/> |Verschieben sie die Unterhaltung.  <br/> |
|Copy  <br/> |Kopieren Sie die Unterhaltung.  <br/> |
|SetReadState  <br/> |Legen Sie den Lesestatus der Unterhaltung fest.  <br/> |
|SetRetentionPolicy  <br/> |Legen Sie die Aufbewahrungsrichtlinie für die Unterhaltung fest.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

