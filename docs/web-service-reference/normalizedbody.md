---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: Das NormalizedBody-Element gibt eine HTML-Darstellung der Body-Eigenschaft eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann.
ms.openlocfilehash: fb249794bccfeed198e7a3230ab53c66893dcf96
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462668"
---
# <a name="normalizedbody"></a>NormalizedBody

Das **NormalizedBody** -Element gibt eine HTML-Darstellung der **Body** -Eigenschaft eines Elements als Fragment an, das in einen anderen HTML-Textkörper eingefügt werden kann. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyType  <br/> |Gibt den Typ des Texts an. Der Wert des **Texts** für das **BodyType** -Attribut gibt an, dass sich der Textkörper in nur-Text-Form befindet. Der Wert von **HTML** für das **BodyType** -Attribut gibt an, dass sich der Text im HTML-Format befindet. Das **BodyType** -Attribut ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Textkörper Inhalt abgeschnitten wurde. Der Textwert **false** für das Attribut **IsTruncated** gibt an, dass der Inhalt des Texts nicht abgeschnitten wurde. Der normalisierte Text wird abgeschnitten, wenn die normalisierte Körperlänge länger ist als der im [MaximumBodySize](maximumbodysize.md) -Element festgelegte Wert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [Aufgabe](task.md)  |  [PostItem](postitem.md)  |  [CalendarItem](calendaritem.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **NormalizedBody** -Elements ist der normalisierte Text des Elements. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

