---
title: WebClientReadFormQueryString
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WebClientReadFormQueryString
api_type:
- schema
ms.assetid: 13e8871a-32a6-4bb9-9493-864c4c07efff
description: Das WebClientReadFormQueryString-Element stellt eine URL dar, die mit dem Outlook Web App Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.
ms.openlocfilehash: 10035aa001c74926ae36e96e09b5b2995844cb68
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538471"
---
# <a name="webclientreadformquerystring"></a>WebClientReadFormQueryString

Das **WebClientReadFormQueryString-Element** stellt eine URL dar, die mit dem Outlook Web App Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen. 
  
```XML
<WebClientReadFormQueryString/>
```

 **Zeichenfolge**
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
|[PostItem](postitem.md) <br/> |Stellt ein Beitragselement im Exchange Informationsspeicher dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine Zeichenfolge darstellt, ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Elementbezeichner für eine Outlook Web App URL ist der EWS-Bezeichner des Elements. Sie können den EWS-Elementbezeichner per URL codieren und an die Abfragezeichenfolge anfügen, um die Outlook Web App-URL für ein Element abzurufen.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
### <a name="version-differences"></a>Versionsunterschiede

Versionen von Exchange, die mit Hauptversion 15 beginnen und mit Exchange Server 2013 Build 15.0.775.38 (CU3) und Exchange Online Version 15.00.0775.009 enden, geben kein korrektes Abfragezeichenfolgenfragment im **WebClientReadFormQueryString-Element** zurück. 
  
In Versionen von Exchange vor der Hauptversion 15 ist der Elementbezeichner für die Outlook Web App URLs ein Outlook Web App Bezeichner. Wenn Sie auf eine Version von Exchange vor der Hauptversion 15 abzielen, müssen Sie den [ConvertId-Vorgang](convertid-operation.md) verwenden, um den Bezeichner zu konvertieren. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

