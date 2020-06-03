---
title: Body
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7851ea9b-9f87-4adc-a26f-7a27df4a9bca
description: Das Body-Element gibt den Textkörper eines Elements an.
ms.openlocfilehash: c565c5701ae5bc210cf0a9dc694108752860e24b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529490"
---
# <a name="body"></a>Body

Das **Body** -Element gibt den Textkörper eines Elements an. 
  
```XML
<Body> BodyType="" IsTruncated="" </Body>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyType  <br/> |Gibt den Typ des Texts an.  <br/> |
|IsTruncated  <br/> |Boolescher Wert, der angibt, ob der Textkörper abgeschnitten ist.  <br/> |
   
#### <a name="bodytype"></a>BodyType

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HTML  <br/> |Gibt an, dass sich der Text im HTML-Format befindet.  <br/> |
|Text  <br/> |Gibt an, dass der Textkörper im Text ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Kontaktelement im Exchange-Speicher.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein generisches Element in der Exchange-Informationsspeicher dar.  <br/> |
|[Meldung](message-ex15websvcsotherref.md) <br/> |Stellt eine Microsoft Exchange e-Mail-Nachricht dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Informationsspeicher dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Body** -Elements ist der Textkörper Inhalt des Elements. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

