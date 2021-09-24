---
title: TokenIssuer (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d7be675-626c-4173-89e9-e32beef81ad5
description: Das TokenIssuer-Element gibt den Uri (SOAP) und den Endpunkt (SOAP) für den Sicherheitstokendienst an.
ms.openlocfilehash: ea1c93493e4f47a6f2551c24586e54614f4f45e6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527265"
---
# <a name="tokenissuer-soap"></a>TokenIssuer (SOAP)

Das **TokenIssuer-Element** gibt den [Uri (SOAP)](uri-soap.md) und [den Endpunkt (SOAP)](endpoint-soap.md) für den Sicherheitstokendienst an. 
  
```XML
<TokenIssuer>
   <Uri/>
   <Endpoint/>
</TokenIssuer>
```

 **TokenIssuer**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Uri (SOAP)](uri-soap.md) <br/> |Der URI des Sicherheitstokendiensts, der das Sicherheitstoken ausgestellt hat.  <br/> |
|[Endpunkt (SOAP)](endpoint-soap.md) <br/> |Der Webdienst-Endpunkt-URI.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TokenIssuers (SOAP)](tokenissuers-soap.md) <br/> |Stellt eine Auflistung von [Sicherheitstokendienst-URI (SOAP)](uri-soap.md) und [Endpunkt (SOAP)](endpoint-soap.md)dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie das **TokenIssuer-Element,** um den Sicherheitstokendienst bei Verwendung von Sicherheitstoken anzugeben. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Name des Schemas  <br/> |AutoErmittlungsschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[AutoErmittlung Webdienstverweis für Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[SOAP AutoDiscover XML-Elemente für Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

