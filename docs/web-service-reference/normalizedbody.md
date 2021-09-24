---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: Das NormalizedBody-Element gibt eine HTML-Darstellung der Body-Eigenschaft eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann.
ms.openlocfilehash: 9ce7a745cfbe2e08afbe4c83873cb670b6afa571
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515432"
---
# <a name="normalizedbody"></a>NormalizedBody

Das **NormalizedBody-Element** gibt eine HTML-Darstellung der **Body-Eigenschaft** eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyType  <br/> |Gibt den Textkörpertyp an. Der Wert von **Text** für das **BodyType-Attribut** gibt an, dass sich der Textkörper in Nur-Text-Form befindet. Der **HTML-Wert** für das **BodyType-Attribut** gibt an, dass sich der Textkörper im HTML-Format befindet. Das **BodyType-Attribut** ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Textkörperinhalt abgeschnitten wurde. Der Textwert **"false"** für das **IsTruncated-Attribut** gibt an, dass der Textkörperinhalt nicht abgeschnitten wurde. Der normalisierte Textkörper wird abgeschnitten, wenn die normalisierte Textkörperlänge länger als der im [MaximumBodySize-Element](maximumbodysize.md) festgelegte Wert ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Aufgabe](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Kontakt](contact.md)  |  [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **NormalizedBody-Elements** ist der normalisierte Textkörper des Elements. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

