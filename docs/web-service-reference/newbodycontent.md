---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: Das NewBodyContent-Element stellt den neuen Textkörperinhalt einer Nachricht dar.
ms.openlocfilehash: 48f6a12e0492249d239196ca3be19857e34e0099
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509515"
---
# <a name="newbodycontent"></a>NewBodyContent

Das **NewBodyContent-Element** stellt den neuen Textkörperinhalt einer Nachricht dar. 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**BodyType** <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht dar.  <br/> |
   
#### <a name="bodytype-attribute"></a>BodyType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**HTML** <br/> |Konvertiert alle Textkörper in HTML.  <br/> |
|**Text** <br/> |Konvertiert alle Textkörper in Nur-Text.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Absender eines Elements im Exchange Speicher.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements im Exchange Speicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Enthält eine Antwort auf ein Beitragselement. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den neuen Textkörperinhalt einer Nachricht dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange Servers, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

