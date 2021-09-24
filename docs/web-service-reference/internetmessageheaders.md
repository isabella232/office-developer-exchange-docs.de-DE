---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: Das InternetMessageHeaders-Element enthält eine Auflistung einiger Internet-Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind. Verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS Eigenschaft, um die gesamte Sammlung von Internetnachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS und Internet-Nachrichtenkopfzeilen finden Sie unterGetting Internet message headersin EWS, MIME, and the missing Internet message headers.
ms.openlocfilehash: 1ea49f2d5cc31aef09a9bc6d38dff25652696842
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541080"
---
# <a name="internetmessageheaders"></a>InternetMessageHeaders

Das **InternetMessageHeaders-Element** enthält eine Auflistung einiger Internet-Nachrichtenkopfzeilen, die in einem Element in einem Postfach enthalten sind. Verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** Eigenschaft, um die gesamte Sammlung von Internetnachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS- und Internet-Nachrichtenkopfzeilen finden Sie unter "Abrufen von Internetnachrichtenkopfzeilen" in [EWS, MIME und den fehlenden Internetnachrichtenkopfzeilen.](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 **NonEmptyArrayOfInternetHeadersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InternetMessageHeader](internetmessageheader.md) <br/> |Stellt den Internetnachrichtenkopf für einen bestimmten Header innerhalb der Headersammlung dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AcceptItem](acceptitem.md) <br/> |Stellt eine Accept-Antwort auf eine Besprechungsanfrage.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DeclineItem](declineitem.md) <br/> |Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Stellt eine Vorbehalt Antwort auf eine Besprechungsanfrage.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es folgt die Definition der erweiterten EWS-API-Eigenschaft für die **PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft.** 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

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


[EWS, MIME und die fehlenden Nachrichtenkopfzeilen](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)

