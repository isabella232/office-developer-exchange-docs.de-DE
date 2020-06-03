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
description: Das NewBodyContent-Element stellt den neuen Textkörper Inhalt einer Nachricht dar.
ms.openlocfilehash: dcfa927bb284ff00e510d8c7b4b31910a70b3cbb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466857"
---
# <a name="newbodycontent"></a>NewBodyContent

Das **NewBodyContent** -Element stellt den neuen Textkörper Inhalt einer Nachricht dar. 
  
```xml
<NewBodyContent BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**BodyType** <br/> |Stellt den tatsächlichen Textinhalt einer Nachricht dar.  <br/> |
   
#### <a name="bodytype-attribute"></a>BodyType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**HTML** <br/> |Wandelt alle Textkörper in HTML um.  <br/> |
|**Text** <br/> |Wandelt alle Textkörper in nur-Text um.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ReplyToItem](replytoitem.md) <br/> |Enthält eine Antwort an den Absender eines Elements in der Exchange-Informationsspeicher.  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |Enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements in der Exchange-Informationsspeicher.  <br/> |
|[ForwardItem](forwarditem.md) <br/> |Enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |Stellt das Antwortobjekt, das Sie eine Besprechung absagen verwendet wird.  <br/> |
|[PostReplyItem](postreplyitem.md) <br/> |Enthält eine Antwort auf ein Post-Element. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den neuen Textkörper Inhalt einer Nachricht dar.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange-Servers, auf dem die Client Zugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

