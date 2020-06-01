---
title: GetUMPropertiesResponse (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: Das GetUMPropertiesResponse-Element definiert eine Antwort auf eine Anforderung des GetUMProperties-Vorgangs (um-Webdienst).
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459125"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (um-Webdienst)

Das **GetUMPropertiesResponse** -Element definiert eine Antwort auf eine Anforderung des [GetUMProperties-Vorgangs (um-Webdienst)](getumproperties-operation-um-web-service.md) . 
  
[GetUMPropertiesResponse (um-Webdienst)](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 **UMProperties**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MissedCallNotificationEnabled (um-Webdienst)](missedcallnotificationenabled-um-web-service.md) <br/> |Gibt an, ob Benachrichtigungen über verpasste Anrufe aktiviert sind.  <br/> |
|[PlayOnPhoneDialString (um-Webdienst)](playonphonedialstring-um-web-service.md) <br/> |Enthält die standardmäßige Wählzeichenfolge, die für den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet werden soll.  <br/> |
|[TelephoneAccessNumbers (um-Webdienst)](telephoneaccessnumbers-um-web-service.md) <br/> |Enthält die Liste der Telefonnummern, die der Benutzer für den Zugriff auf Unified Messaging über ein Telefon verwenden kann.  <br/> |
|[TelephoneAccessFolderEmail (um-Webdienst)](telephoneaccessfolderemail-um-web-service.md) <br/> |Enthält den Bezeichner für den e-Mail-Ordner, aus dem Unified Messaging Nachrichten über das Telefon lesen kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (um-Webdienst)](getumproperties-operation-um-web-service.md)

