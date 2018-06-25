---
title: WebClientReadFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: Das WebClientReadFormQueryString-Element stellt eine URL zu verketten an den Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.
ms.openlocfilehash: 8096c14956d132a631b0ade6f2eae12a2bff9c06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839519"
---
# <a name="webclientreadformquerystring"></a>WebClientReadFormQueryString

Das **WebClientReadFormQueryString** -Element stellt eine URL zu verketten an den Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen. 
  
```XML
<WebClientReadFormQueryString/>
```

 **string**
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
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[PostItem-Objekt](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Speicher.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Die Element-ID für ein Outlook Web App-URL ist der EWS-Bezeichner des Elements. Können die URL-Kodierung der EWS-Elementbezeichner und fügen Sie es an die Abfragezeichenfolge zum Abrufen der Outlook Web App-URL für ein Element.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
### <a name="version-differences"></a>Versionsunterschiede

Versionen von Exchange mit Hauptversion 15 beginnend und endend mit Exchange Server 2013 erstellen 15.0.775.38 (CU3) und Exchange Online Version 15.00.0775.009 ein Fragment einer korrekte Abfrage nicht im **WebClientReadFormQueryString** -Element zurück. 
  
In früheren Versionen von Exchange als Hauptversion 15 ist der Bezeichner für die Outlook Web App-URLs ein Outlook Web App-Bezeichner. Wenn Sie eine Version von Exchange vor Hauptversion 15 abzielen, müssen Sie den [Vorgang ConvertId](convertid-operation.md) verwenden, um den Bezeichner zu konvertieren. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

