---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: Das InternetMessageHeader-Element stellt den Internet Nachrichtenkopf für eine bestimmte Kopfzeile in der Headers-Auflistung dar. Verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS-und Internet Nachrichtenkopfzeilen, unterkauf-Internet Nachrichtenkopfzeilen in EWS, MIME und die fehlenden Internet Nachrichtenkopfzeilen.
ms.openlocfilehash: 7b662617e0b1a1fcdcce3449b729485ba6e0956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459307"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

Das **InternetMessageHeader** -Element stellt den Internet Nachrichtenkopf für eine bestimmte Kopfzeile in der Headers-Auflistung dar. Verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft, um die gesamte Auflistung von Internet Nachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Getting Internet Message Headers in [EWS, MIME, and the Missing Internet Message](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)Headers.
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Headername** <br/> |Gibt den Namen des Headers an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt den Wert für den Header dar.
  
## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die verwaltete EWS-API erweiterte Eigenschaftsdefinition für die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft. 
  
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

