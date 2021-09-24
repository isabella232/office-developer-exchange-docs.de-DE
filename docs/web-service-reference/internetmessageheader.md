---
title: InternetMessageHeader
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- InternetMessageHeader
api_type:
- schema
ms.assetid: c70675f8-6feb-4c89-ba48-bce0479b308b
description: Das InternetMessageHeader-Element stellt den Internetnachrichtenkopf für einen bestimmten Header innerhalb der Headersammlung dar. Verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS Eigenschaft, um die gesamte Sammlung von Internetnachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS und Internet-Nachrichtenkopfzeilen finden Sie unterGetting internet message headers in EWS, MIME, and the missing Internet message headers.
ms.openlocfilehash: 4b3072611e8a3debf87ce2a023f4f68ee4487185
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541084"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

Das **InternetMessageHeader-Element** stellt den Internetnachrichtenkopf für einen bestimmten Header innerhalb der Headersammlung dar. Verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** Eigenschaft, um die gesamte Sammlung von Internetnachrichtenkopfzeilen abzurufen. Weitere Informationen zu EWS- und Internet-Nachrichtenkopfzeilen finden Sie unter "Abrufen von Internetnachrichtenkopfzeilen in [EWS, MIME und den fehlenden Internetnachrichtenkopfzeilen.](https://msdn.microsoft.com/library/exchange/hh545614%28v=exchg.140%29.aspx)
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Headername** <br/> |Gibt den Namen der Kopfzeile an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internetnachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Wert für die Kopfzeile dar.
  
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

