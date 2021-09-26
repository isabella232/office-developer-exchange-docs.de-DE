---
title: WebClientUrl (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 7f8cb6d6-4aac-4a1f-8bec-2dcb90fc1df6
description: Das WebClientUrl-Element stellt die URL eines Exchange Webclients dar.
ms.openlocfilehash: 73cc03411e8356fafe078df45f9ebd695e8f154b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542596"
---
# <a name="webclienturl-soap"></a>WebClientUrl (SOAP)

Das **WebClientUrl-Element** stellt die URL eines Exchange Webclients dar. 
  
[UserSetting (SOAP)](usersetting-soap.md)
  
[WebClientUrls (SOAP)](webclienturls-soap.md)
  
[WebClientUrl (SOAP)](webclienturl-soap.md)
  
```XML
<WebClientUrl>
    <AuthenticationMethods/>
    <Url/>
</WebClientUrl>
```

 **WebClientUrl**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AuthenticationMethods (SOAP)](authenticationmethods-soap.md) <br/> |Stellt die Authentifizierungsmethode dar, die beim Zugriff auf die angegebene URL verwendet werden soll.  <br/> |
|[Url (SOAP)](url-soap.md) <br/> |Stellt die Webadresse für die URL dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[WebClientUrls (SOAP)](webclienturls-soap.md) <br/> |Stellt eine Benutzereinstellung dar, die eine Auflistung von **WebClientUrl-Elementen** enthält.  <br/> |
   
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Url (SOAP)](url-soap.md)
  
[WebClientUrls (SOAP)](webclienturls-soap.md)

