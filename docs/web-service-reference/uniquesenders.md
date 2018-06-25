---
title: UniqueSenders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueSenders
api_type:
- schema
ms.assetid: 1f55f2fe-b2f2-4169-83c1-fa5c752bd695
description: Das UniqueSenders-Element enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: b75846534141e23e6d8158bc36f0ef60bcb1d7ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839313"
---
# <a name="uniquesenders"></a>UniqueSenders

Das **UniqueSenders** -Element enthält eine Liste von allen Absendern von Unterhaltungselementen im aktuellen Ordner. Dieses Element ist schreibgeschützt. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
[UniqueSenders](uniquesenders.md)
  
```XML
<UniqueSenders>
   <String/>
</UniqueSenders>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[String](string.md) <br/> |Enthält einen einzelnen Gespräch Absender.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
   
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

