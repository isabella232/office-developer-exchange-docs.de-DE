---
title: GetUMPropertiesResponse (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: Das GetUMPropertiesResponse-Element definiert eine Antwort auf eine GetUMProperties-Vorgangsanforderung (UM-Webdienst).
ms.openlocfilehash: 97c3850d46369d4ab533629a8b24e199db3dd44a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522964"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (UM-Webdienst)

Das **GetUMPropertiesResponse-Element** definiert eine Antwort auf eine [GetUMProperties-Vorgangsanforderung (UM-Webdienst).](getumproperties-operation-um-web-service.md) 
  
[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md)
  
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
|[MissedCallNotificationEnabled (UM-Webdienst)](missedcallnotificationenabled-um-web-service.md) <br/> |Gibt an, ob Benachrichtigungen über verpasste Anrufe aktiviert sind.  <br/> |
|[PlayOnPhoneDialString (UM-Webdienst)](playonphonedialstring-um-web-service.md) <br/> |Enthält die Standardwählzeichenfolge, die für den [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet werden soll.  <br/> |
|[TelephoneAccessNumbers (UM-Webdienst)](telephoneaccessnumbers-um-web-service.md) <br/> |Enthält die Liste der Telefonnummern, die der Benutzer für den Zugriff auf Unified Messaging über ein Telefon verwenden kann.  <br/> |
|[TelephoneAccessFolderEmail (UM-Webdienst)](telephoneaccessfolderemail-um-web-service.md) <br/> |Enthält den Bezeichner für den E-Mail-Ordner, aus dem Unified Messaging Nachrichten über das Telefon liest.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md)

