---
title: Unterhaltung (ConversationRequestType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0308b71c-d4ff-44a8-b9ca-d5965291ee1d
description: Das Conversation-Element stellt eine einzelne Unterhaltung dar, die in einer GetConversationItems-Antwort zurückgegeben wird.
ms.openlocfilehash: 9c7faf9c06c1476bca688e831f452e711a89f10f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533893"
---
# <a name="conversation-conversationrequesttype"></a>Unterhaltung (ConversationRequestType)

Das **Conversation-Element** stellt eine einzelne Unterhaltung dar, die in einer **GetConversationItems-Antwort** zurückgegeben wird. 
  
```XML
<Conversation>
   <ConversationId/>
   <SyncState/>
</Conversation>
```

 ****
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ConversationId](conversationid.md)  |  [SyncState (base64Binary)](syncstate-base64binary.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Unterhaltungen](conversations-ex15websvcsotherref.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

