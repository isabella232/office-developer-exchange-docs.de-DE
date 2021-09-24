---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: Das FindConversation-Element definiert eine Anforderung zum Suchen nach Unterhaltungen in einem Postfach.
ms.openlocfilehash: e48e0d9fd71dac12fe6848031b2c056ea9a913ce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535170"
---
# <a name="findconversation"></a>FindConversation

Das **FindConversation-Element** definiert eine Anforderung zum Suchen nach Unterhaltungen in einem Postfach. 
  
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
|Traversal  <br/> |Identifiziert die Typen der Untergeordneten Strukturdurchquerung. Dieses Attribut ist optional.  <br/> |
|ViewFilter  <br/> |Identifiziert die Typenansichtsfilter. Dieses Attribut ist optional.  <br/> |
   
#### <a name="traversal-attribute-values"></a>Traversalattributwerte

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Flachen  <br/> |Gibt einen flachen Traversal an.  <br/> |
|Tief  <br/> |Gibt eine tiefe Durchquerung an.  <br/> |
   
#### <a name="viewfilter-attribute-values"></a>ViewFilter-Attributwerte

****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Alle  <br/> |Suchen Sie alle Unterhaltungen.  <br/> |
|Gekennzeichnet  <br/> |Markierte Unterhaltungen suchen.  <br/> |
|HasAttachment  <br/> |Suchen von Unterhaltungen mit Anlagen.  <br/> |
|ToOrCcMe  <br/> |Suchen Sie an mich adressierte Unterhaltungen oder "cc'd".  <br/> |
|Ungelesen  <br/> |Ungelesene Unterhaltungen suchen.  <br/> |
|TaskActive  <br/> |Suchen sie nach aktiven Vorgängen.  <br/> |
|TaskOverdue  <br/> |Suchen sie überfällige Aufgaben.  <br/> |
|TaskCompleted  <br/> |Nach abgeschlossenen Aufgaben suchen.  <br/> |
|NoClutter  <br/> |Ausschließlich für interne Zwecke.  <br/> |
|Unwichtige Elemente  <br/> |Ausschließlich für interne Zwecke.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IndexedPageItemView](indexedpageitemview.md) <br/> |Beschreibt, wie Seitenunterhaltungsinformationen zurückgegeben werden.  <br/> |
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Gibt die Bedingung an, die verwendet wird, um das Ende einer Suche, den Startindex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für eine **FindItem-** oder **FindConversation-Suche** zu identifizieren.  <br/> |
|[SortOrder](sortorder.md) <br/> |Definiert, wie Elemente in einer [FindConversation-Vorgangsanforderung](findconversation-operation.md) sortiert werden. Die **conversation:LastDeliveryTime-Eigenschaft** ist die einzige Eigenschaft, die für die Sortierung unterstützt wird, wenn der **FindConversation-Vorgang** verwendet wird.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifiziert den Ordner, in dem nach Unterhaltungen gesucht werden soll.  <br/> |
|[MailboxScope](mailboxscope.md) <br/> |Gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder das primäre postfach und das Archivpostfach umfassen soll.  <br/> |
|[QueryString (QueryStringType)](querystring-querystringtype.md) <br/> |Gibt eine Postfachabfragezeichenfolge basierend auf der erweiterten Abfragesyntax (Advanced Query Syntax, AQS) an.  <br/> |
|[ConversationShape](conversationshape.md) <br/> |Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation-Vorgang](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

