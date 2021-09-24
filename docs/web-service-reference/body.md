---
title: Body
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: Das Body-Element gibt den Textkörper eines Elements an.
ms.openlocfilehash: 47f0726c6ef329fbbefc99be3b1e2d605f852afa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526848"
---
# <a name="body"></a>Text

Das  Body-Element gibt den Textkörper eines Elements an. 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyType  <br/> |Gibt den Typ des Textkörpers an.  <br/> |
|IsTruncated  <br/> |Boolescher Wert, der angibt, ob der Textkörper abgeschnitten ist.  <br/> |
   
#### <a name="bodytype"></a>BodyType

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HTML  <br/> |Gibt an, dass sich der Textkörper in HTML befindet.  <br/> |
|Text  <br/> |Gibt an, dass sich der Textkörper im Text befindet.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Kontaktelement im Exchange-Speicher.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Aspekt](item.md) <br/> |Stellt ein generisches Element im Exchange Speicher dar.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine Microsoft Exchange-E-Mail-Nachricht dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Beitragselement im Exchange Informationsspeicher dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Body-Elements** ist der Textinhalt des Elements. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

