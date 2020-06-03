---
title: HasAttachments
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasAttachments
api_type:
- schema
ms.assetid: 538b7a85-11d7-4daa-8458-09b540760e8b
description: Das Element HasAttachments stellt eine Eigenschaft, die auf true festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar hat oder wenn eine Unterhaltung mit mindestens ein Element enthält, die eine Anlage enthält. Diese Eigenschaft ist schreibgeschützt.
ms.openlocfilehash: cc4e4ec0eac1c749723facc8cd780da41b0d8150
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462922"
---
# <a name="hasattachments"></a>HasAttachments

Das Element **HasAttachments** stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar hat oder wenn eine Unterhaltung mit mindestens ein Element enthält, die eine Anlage enthält. Diese Eigenschaft ist schreibgeschützt. 
  
```XML
<HasAttachments/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen, die beim erfüllt, wird die Regelaktionen für diese Regel ausgelöst.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt alle verfügbaren Regel Ausnahmebedingungen für die Posteingangsregel an.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich. Der Wert **true** bedeutet, dass das Element oder eine Unterhaltung mindestens eine Anlage sichtbar hat. Ein Wert **false** bedeutet, dass das Element oder die Unterhaltung keine Anlagen enthält auf, oder nur Anlagen ausgeblendet wurde. 
  
## <a name="remarks"></a>Bemerkungen

Die **HasAttachments** -Eigenschaft wird von der MAPI-Eigenschaft vom Typ Boolean **AllAttachmentsHidden** berechnet. Wenn ein Element eine Anlage nicht verfügt, wird die **AllAttachmentsHidden** -Eigenschaft ist nicht vorhanden. Wenn alle Anlagen für das Element ausgeblendet sind, ist die **AllAttachmentsHidden** -Eigenschaft **true**. Die **AllAttachmentsHidden** -Eigenschaft ist **false**, wenn sie mindestens eine Anlage hat und mindestens einer der Anlagen sichtbar ist. Verwenden Sie die **AllAttachmentsHidden** MAPI-Eigenschaft für suchen, gruppieren und Sortieren von Elementen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
[EWS-Referenz für Exchange](ews-reference-for-exchange.md)

