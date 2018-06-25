---
title: GetUMPropertiesResponse (UM-Webdienst)
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
description: Das GetUMPropertiesResponse-Element definiert eine Antwort auf eine GetUMProperties-Vorgang (UM-Webdienst) an.
ms.openlocfilehash: c0df872ad6b8e6541fa750ab87f4c1e5f0118b00
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829685"
---
# <a name="getumpropertiesresponse-um-web-service"></a>GetUMPropertiesResponse (UM-Webdienst)

Das **GetUMPropertiesResponse** -Element definiert eine Antwort auf eine [GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md) an. 
  
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
|[PlayOnPhoneDialString (UM-Webdienst)](playonphonedialstring-um-web-service.md) <br/> |Enthält die Standardzeichenfolge Zugriffsnummern für den [PlayOnPhone Betrieb (UM-Webdienst)](playonphone-operation-um-web-service.md) und [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwenden.  <br/> |
|[TelephoneAccessNumbers (UM-Webdienst)](telephoneaccessnumbers-um-web-service.md) <br/> |Enthält die Liste von Telefonnummern, mit denen der Benutzer über ein Telefon Zugriff auf Unified Messaging.  <br/> |
|[TelephoneAccessFolderEmail (UM-Webdienst)](telephoneaccessfolderemail-um-web-service.md) <br/> |Enthält den Bezeichner für den e-Mail-Ordner aus dem Unified Messaging Nachrichten über das Telefon gelesen werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUMProperties-Vorgang (UM-Webdienst)](getumproperties-operation-um-web-service.md)

