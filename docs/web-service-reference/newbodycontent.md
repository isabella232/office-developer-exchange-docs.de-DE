---
title: NewBodyContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NewBodyContent
api_type:
- schema
ms.assetid: 0303600d-16d8-4685-88f2-980c5ca7e9a6
description: Das NewBodyContent-Element darstellt, den neuen Body-Inhalt einer Nachricht.
ms.openlocfilehash: b87393e460b1eee1c13efebf38e898d17915bd71
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830516"
---
# <a name="newbodycontent"></a>NewBodyContent

Das **NewBodyContent** -Element darstellt, den neuen Body-Inhalt einer Nachricht. 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**BodyType** <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht.  <br/> |
   
#### <a name="bodytype-attribute"></a>BodyType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**HTML** <br/> |Konvertiert alle Texte in HTML.  <br/> |
|**Text** <br/> |Alle Texte konvertiert in nur-Text.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Absender eines Elements in der Exchange-Speicher.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an den Absender und alle gefundenen Empfänger eines Elements in der Exchange-Speicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Eine Antwort auf eine Post-Element enthält. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den neuen Textkörperinhalt einer Nachricht.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Exchange-Servers, der die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

