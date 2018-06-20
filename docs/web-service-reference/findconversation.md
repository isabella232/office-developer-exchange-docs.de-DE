---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: Das FindConversation-Element definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758439"
---
# <a name="findconversation"></a>FindConversation

Das **FindConversation** -Element definiert eine Anforderung an Unterhaltungen in einem Postfach suchen. 
  
[FindConversation](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 **FindConversationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

****

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Durchqueren  <br/> |Identifiziert die Typen der Teilstruktur durchqueren. Dieses Attribut ist optional.  <br/> |
|ViewFilter  <br/> |Identifiziert die Typen Ansichtsfilter. Dieses Attribut ist optional.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal Attributwerte

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flach  <br/> |Gibt eine flache durchqueren an.  <br/> |
|Tief  <br/> |Gibt eine Tiefe durchqueren an.  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>Attributwerte ViewFilter

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Hier finden Sie alle Unterhaltungen.  <br/> |
|Gekennzeichnet  <br/> |Hier finden Sie gekennzeichnete Unterhaltungen.  <br/> |
|HasAttachment  <br/> |Hier finden Sie Unterhaltungen mit Anlagen.  <br/> |
|ToOrCcMe  <br/> |Hier finden Sie Unterhaltungen adressierte oder "Cc" mir würde.  <br/> |
|Unread  <br/> |Hier finden Sie ungelesene Unterhaltungen.  <br/> |
|TaskActive  <br/> |Suchen Sie nach aktiven Vorgänge.  <br/> |
|TaskOverdue  <br/> |Hier finden Sie überfällige Aufgaben angezeigt.  <br/> |
|Aufruft  <br/> |Suchen Sie nach abgeschlossenen Aufgaben.  <br/> |
|NoClutter  <br/> |Nur für internen Gebrauch.  <br/> |
|Unübersichtlichkeit  <br/> |Nur für internen Gebrauch.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie ausgelagerten Unterhaltung Informationen zurückgegeben.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Gibt die Bedingung an, die zur Identifizierung der am Ende von einer Suche, der Startindex für eine Suche, die maximale Einträge zurückgegeben und die Suche erfahren Sie, wie eine Suche **FindItem** oder **FindConversation** verwendet wird.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer Anforderung [FindConversation Vorgang](findconversation-operation.md) sortiert werden. Die **Unterhaltung: LastDeliveryTime** -Eigenschaft ist die einzige Eigenschaft, die unterstützt werden, für die Sortierung, wenn der Vorgang **FindConversation** verwendet wird.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifiziert den Ordner nach Unterhaltungen suchen.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Gibt an, ob eine Suche oder Fetch für eine Unterhaltung das primäre Postfach, Archivpostfach oder den Primär-umfassen und Postfach archivieren soll.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Gibt ein Postfach Abfragezeichenfolge basierend auf Erweiterte Query Syntax (AQS) an.  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Bezeichnet die Eigenschaft festgelegt, dass in einer Antwort [FindConversation Vorgang](findconversation-operation.md) zurückgegeben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation Operation](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Conversations in EWS](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

