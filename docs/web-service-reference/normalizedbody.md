---
title: NormalizedBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfb813e4-642d-4f1b-9e91-1fee89dbd083
description: Das NormalizedBody-Element gibt eine HTML-Darstellung der die Body-Eigenschaft eines Elements als Fragment, das in einem anderen HTML-Text eingefügt werden kann.
ms.openlocfilehash: 07c2176d2c8a7473c06b7e42f8bcbbe6670581ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830548"
---
# <a name="normalizedbody"></a>NormalizedBody

Das **NormalizedBody** -Element gibt eine HTML-Darstellung der die **Body** -Eigenschaft eines Elements als Fragment, das in einem anderen HTML-Text eingefügt werden kann. 
  
```XML
<NormalizedBody BodyType="Text | HTML" IsTruncated="true | false"></NormalizedBody>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|BodyType  <br/> |Gibt den Typ des Hauptteils an. Der Wert der **Text** für das **BodyType** -Attribut gibt an, dass der Text in nur-Text-Format ist. Der Wert von **HTML** für das **BodyType** -Attribut gibt an, dass der Textkörper in HTML-Formular ist. Das Attribut **BodyType** ist erforderlich.  <br/> |
|IsTruncated  <br/> |Gibt an, dass der Inhalt des Body abgeschnitten worden sein. Der Textwert **false** für das **IsTruncated** -Attribut gibt an, dass der Inhalt des Body nicht abgeschnitten worden sein. Normalisierte Textkörper werden abgeschnitten, wenn die normalisierte Textkörper Länge länger als der Wert im [MaximumBodySize](maximumbodysize.md) -Element festgelegt ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Element](item.md) | [Nachricht](message-ex15websvcsotherref.md) | [MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [Aufgabe](task.md) | [PostItem-Objekt ](postitem.md)  |  [CalendarItem](calendaritem.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **NormalizedBody** -Elements ist die normalisierte Textkörper des Elements. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

