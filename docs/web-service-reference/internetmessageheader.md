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
description: Das InternetMessageHeader-Element darstellt, den Internet Nachrichtenkopf für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung. Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die PR_TRANSPORT_MESSAGE_HEADERS-Eigenschaft. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen, SeeGetting Internet-Nachrichtenköpfe in EWS MIME und fehlenden Internetkopfzeilen Nachricht.
ms.openlocfilehash: 9457cdabe99c0adcb8183cbc039cc86db881fec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829952"
---
# <a name="internetmessageheader"></a>InternetMessageHeader

Das **InternetMessageHeader** -Element darstellt, den Internet Nachrichtenkopf für einen angegebenen Header innerhalb der Kopfzeilen-Auflistung. Wenn Sie die gesamte Auflistung der Internetkopfzeilen Nachricht erhalten möchten, verwenden Sie die **PR_TRANSPORT_MESSAGE_HEADERS** -Eigenschaft. Weitere Informationen zu EWS und Internet Nachrichtenkopfzeilen finden Sie unter "Nachrichtenkopfzeilen in [EWS, MIME, und die fehlenden Internet Nachrichtenkopfzeilen](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)Internet abrufen.
  
```XML
<InternetMessageHeader HeaderName=""/>
```

 **InternetHeaderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**HeaderName** <br/> |Gibt den Kopfzeilennamen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert steht für den Wert für die Kopfzeile.
  
## <a name="remarks"></a>Hinweise

Es folgt die EWS Managed API erweiterten Eigenschaftendefinition für die Eigenschaft **PR_TRANSPORT_MESSAGE_HEADERS** . 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[EWS, MIME und die fehlenden Nachrichtenkopfzeilen](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

