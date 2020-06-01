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
description: Das FindConversation-Element definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.
ms.openlocfilehash: 98d692132ed9375d981c95d24600b0e2c4b1d8c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462647"
---
# <a name="findconversation"></a>FindConversation

Das **FindConversation** -Element definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach. 
  
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
|Traversal  <br/> |Gibt die Typen der Unterstruktur Traversal an. Dieses Attribut ist optional.  <br/> |
|ViewFilter  <br/> |Identifiziert die Typen Ansichtsfilter. Dieses Attribut ist optional.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversal-Attributwerte

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Gibt eine flache Durchquerung an.  <br/> |
|Tiefe  <br/> |Gibt einen tiefen Durchlauf an.  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>ViewFilter-Attributwerte

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Suchen Sie nach allen Unterhaltungen.  <br/> |
|Gekennzeichnet  <br/> |Suchen nach gekennzeichneten Unterhaltungen.  <br/> |
|HasAttachment  <br/> |Unterhaltungen mit Anlagen suchen.  <br/> |
|ToOrCcMe  <br/> |Hier finden Sie Unterhaltungen, die an mich gerichtet oder CC 'd.  <br/> |
|Ungelesen  <br/> |Suchen Sie nach ungelesenen Unterhaltungen.  <br/> |
|TaskActive  <br/> |Suchen Sie nach aktiven Aufgaben.  <br/> |
|TaskOverdue  <br/> |Überfällige Vorgänge suchen.  <br/> |
|TaskCompleted  <br/> |Finden Sie abgeschlossene Aufgaben.  <br/> |
|Noclutter  <br/> |Ausschließlich für interne Zwecke.  <br/> |
|Unwichtige Elemente  <br/> |Ausschließlich für interne Zwecke.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie Informationen zur ausgelagerten Unterhaltung zurückgegeben werden.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Gibt die Bedingung an, die zum Identifizieren des Endes einer Suche, des startIndex einer Suche, der maximal zurückzugebenden Einträge und der Suchanweisungen für eine **FindItem** -oder **FindConversation** -Suche verwendet wird.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer [FindConversation-Vorgangs](findconversation-operation.md) Anforderung sortiert werden. Die **Conversation: LastDeliveryTime** -Eigenschaft ist die einzige Eigenschaft, die beim Verwenden des **FindConversation** -Vorgangs für die Sortierung unterstützt wird.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Gibt den Ordner an, in dem nach Unterhaltungen gesucht werden soll.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Gibt an, ob sich eine Suche oder ein Abruf für eine Unterhaltung entweder auf das primäre Postfach, das Archivpostfach oder sowohl auf das primäre als auch auf das Archivpostfach erstrecken soll.  <br/> |
|[QueryString (querystringtype)](querystring-querystringtype.md) <br/> |Gibt eine Post Fach Abfragezeichenfolge basierend auf der erweiterten Abfrage Syntax (AQS) an.  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Gibt den Eigenschaftensatz an, der in einer [FindConversation-Vorgangs](findconversation-operation.md) Antwort zurückgegeben werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation-Vorgang](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

